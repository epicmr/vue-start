<template>
  <div>
    <Lesson8>
      <template #header="data">
        <option :key="item" v-for="item in data.items">{{item}}</option>
      </template>
    </Lesson8>
  </div>
</template>

<script>
import Lesson8 from './components/Lesson8.vue'

export default {
  name: 'App',
  data () {
    return {
    }
  },
  components: {
    Lesson8
  },
  methods: {
    changeSubmit (event) {
      console.log(event.target.value)
    }
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
