<template>
  <div class="chat-input">
    <input type="text" placeholder="메시지를 입력하세요..." />
    <button class="btn">전송</button>
  </div>
</template>

<style scoped>
/* 채팅 입력창 스타일 */
.chat-input {
  margin-top: 10px;
}

/* 입력창 및 버튼 스타일 */
.chat-input input[type="text"] {
  width: 70%;
  padding: 10px;
  font-size: 14px;
  border-radius: 5px 0 0 5px;
  border: 1px solid #ccc;
  outline: none;
}

.chat-input .btn {
  padding: 10px;
  background-color: #4caf50;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 0 5px 5px 0;
}
</style>
