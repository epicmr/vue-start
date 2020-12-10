<template>
  <div>
    <div>
      <span :title="message">鼠标移到这里看看</span>
    </div>
    <div>
      <span>{{message}}</span>
    </div>
    <div>
      <input type="text"
             v-model="message">
    </div>
    <button @click="click">点这里试试</button>
  </div>
</template>

//基础模板
<script>
import { setInterval } from 'timers';
export default {
  name: 'Lesson2',
  props: {
    msg: String
  },
  data () {
    return {
      message: "你看到的是我想让你看到的！"
    }
  },
  methods: {
    click () {
      this.message = this.message.split('').reverse().join('')
    }
  },
  mounted () {
    setInterval(
      () => {
        this.counter++
      }, 1000)
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
