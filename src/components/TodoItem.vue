<template>
  <li>{{todo.name}}</li>
</template>

//基础模板
<script>
export default {
  name: 'TodoItem',
  props: {
    todo: Object
  },
  data () {
    return {
    }
  },
  mounted () {
  },
  methods: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
