<template>
  <div>
    <input type="text">
    <select name="select" id="select">
      <option :key="item" :value="item" v-for="item in items">{{item}}</option>
    </select>
  </div>
</template>

//props
<script>
export default {
  name: 'Lesson1',
  data () {
    return {
      counter: 0,
      items: ["oringe", "apple", "banana"]
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
  },
  created () {
    console.log("attrs", this.$attrs)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
