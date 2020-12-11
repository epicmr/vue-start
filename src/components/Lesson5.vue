<template>
  <div>
    <input type="text">
  </div>
</template>

//基础模板
<script>
import { setInterval } from 'timers';
export default {
  name: 'Lesson5',
  data () {
    return {
      question: "",
      answer: {}
    }
  },
  props: {
    msg: String
  },
  computed: {
  },
  methods: {
  },
  mounted () {
    setInterval(
      () => {
        this.counter++
      }, 1000)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
