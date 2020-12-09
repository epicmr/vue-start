<template>
<div>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Lesson1></Lesson1>
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Lesson1 from './components/Lesson1.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Lesson1
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
