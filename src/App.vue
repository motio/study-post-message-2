<template>
  <div id="app">
    <h1>送信側</h1>
    <button @click="submit">送信</button>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      msg: '送られたテキスト',
    };
  },
  methods: {
    submit() {
      window.parent.postMessage(this.msg, 'http://localhost:5000');
    },
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
