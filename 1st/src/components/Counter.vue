<template>
    <div>
      <!-- counter変数を格納しよう -->
      <h1>Counter: {{ counter }}</h1>
      <!-- ボタンを配置しよう -->
      <button @click="increment">Increment</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        counter: 0
      };
    },
    methods: {
      <!-- ボタンが押されると増えるようにしよう -->
      increment() {
        this.counter++;
      }
    }
  };
  </script>
  