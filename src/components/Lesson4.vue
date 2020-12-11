<template>
  <div>
    <p>
      <span>{{author.age}}</span>
    </p>
    <p>
      <span>{{methodAge()}}</span>
    </p>
    <p>
      <span>{{computedAge}}</span>
    </p>
    <p>
      <button @click="author.age++">点这里试试</button>
    </p>
  </div>
</template>

//计算属性和函数
//计算属性每次依赖项发生变化时才会重新计算，属于有缓存
//函数是每次触发重新渲染时就会重新计算，属于无缓存
<script>
import { setInterval } from 'timers';

export default {
  name: 'Lesson4',
  props: {
    msg: String
  },
  data () {
    return {
      author: {
        name: "pnh",
        age: 10,
        books: [
          "vue1 sss",
          "vue2 kkk",
          "vue3 uuu"
        ]
      }
    }
  },
  methods: {
    methodAge () {
      return Date.now() % 2 == 0 ? "yes" : "no"
    }
  },
  computed: {
    computedAge () {
      return Date.now() % 2 == 0 ? "yes" : "no"
    }
  },
  mounted () {
    setInterval(() => {
      this.author.age++
    }, 1000)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
