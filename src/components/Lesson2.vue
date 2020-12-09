<template>
  <div>
      Counter:{{counter}}
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
  data() {
      return {
          counter:0
      }
  },
  mounted() {
      setInterval(
          () =>{
              this.counter++
        },1000)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
