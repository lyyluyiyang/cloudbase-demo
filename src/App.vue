<template>
  <div class="app">
    <h1>CloudBase 演示应用</h1>
    <p>这是一个使用 Vue 3 和 CloudBase 构建的演示应用</p>
    <button @click="login">登录</button>
  </div>
</template>

<script>
import { auth } from '@cloudbase/js-sdk'

export default {
  name: 'App',
  methods: {
    login() {
      const app = auth()
      app.toDefaultLoginPage()
    }
  }
}
</script>

<style scoped>
.app {
  text-align: center;
  margin-top: 60px;
}

button {
  padding: 10px 20px;
  background: #007aff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
</style>