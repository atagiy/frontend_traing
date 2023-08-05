
<template>
    <div>
      <!-- テキストボックスに入力した内容を表示 -->
      <input type="text" v-model="inputText">
      <button @click="sendMessage">送信</button>
  
      <!-- バックエンドからのレスポンスを表示 -->
      <p v-if="response">{{ response }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        inputText: '', // テキストボックスに入力した内容を保持するデータ
        response: '', // バックエンドからのレスポンスを保持するデータ
      };
    },
    methods: {
      sendMessage() {
        // ここで実際にバックエンドにテキストを送信する処理を行う
        // 以下はサンプルとして、送信した内容をそのままレスポンスとして表示する
        this.response = '送信された内容: ' + this.inputText;
      },
    },
  };
  </script>
  