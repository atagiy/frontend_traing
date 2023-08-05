<template>
  <img alt="Vue logo" src="./assets/aitc.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
// コーポネントをインポートしてみよう！
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // コーポネントを追加してみよう！
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  /* 背景色を指定（例：青色） */
  background-color: #f1d9f5;
}
</style>
