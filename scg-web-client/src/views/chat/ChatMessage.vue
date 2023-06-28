<template>
  <div :class="['chat-message', messageClass]">
    <div class="chat-profile">
      <img :src="profileImage" :alt="username + '의 프로필 사진'" />
      <span class="chat-username">{{ username }}</span>
    </div>
    <p>{{ message }}</p>
    <span class="chat-time">{{ time }}</span>
  </div>
</template>

<script>
export default {
  props: {
    messageClass: String,
    profileImage: String,
    username: String,
    message: String,
    time: String,
  },
};
</script>

<style scoped>
/* 개별 채팅 메시지 스타일 */
.chat-message {
  margin-bottom: 10px;e
  padding: 10px;
  border-radius: 5px;
  font-size: 14px;
  line-height: 1.4;
}

/* 상대방 메시지 스타일 */
.chat-message.other {
  background-color: #ffffff;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
}

/* 내 메시지 스타일 */
.chat-message.self {
  background-color: #e2f7fd;
  text-align: right;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
}

.chat-time {
  font-size: 12px;
  color: #999;
  margin-top: 5px;
}

/* 채팅 프로필 스타일 */
.chat-profile {
  display: flex;
  align-items: center;
  margin-bottom: 5px;
}

.chat-profile img {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  margin-right: 5px;
}

.chat-username {
  font-weight: bold;
}
</style>
