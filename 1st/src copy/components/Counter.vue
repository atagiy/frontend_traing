<template>
    <div>
      <h1>Counter: {{ counter }}</h1>
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
      increment() {
        this.counter++;
      }
    }
  };
  </script>
  