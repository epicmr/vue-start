<template>
  <div>
    <span v-if="seen">{{message}}</span>
    <div>
      <button @click="click">点这里试试</button>
    </div>
    <div>
      <ol>
        <todo-item :key="item.name"
                   :todo="item"
                   v-for="item in todos">
        </todo-item>
      </ol>
    </div>
  </div>
</template>

//基础模板
<script>
import { TodoItem } from './TodoItem.vue'
export default {
  name: 'Lesson3',
  components: {
    TodoItem
  },
  props: {
    msg: String
  },
  data () {
    return {
      seen: true,
      message: "变魔术咯！",
      todos: [
        { "name": "苹果", "color": "红色" },
        { "name": "雪梨", "color": "白色" },
        { "name": "香蕉", "color": "黄色" },
      ]
    }
  },
  mounted () {
  },
  methods: {
    click () {
      this.seen = !this.seen
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
