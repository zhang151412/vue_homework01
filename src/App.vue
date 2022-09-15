<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <BookMgr msg="图书管理系统"/>
</template>

<script>
import BookMgr from './components/BookMgr.vue'

export default {
  name: 'App',
  components: {
    BookMgr
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
}
</style>
