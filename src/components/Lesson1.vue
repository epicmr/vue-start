<template>
  <div>
    Counter:{{counter}}
  </div>
</template>

//基础模板
<script>
import { setInterval } from 'timers';
export default {
  name: 'Lesson1',
  data () {
    return {
      counter: 0
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
