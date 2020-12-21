 <template>
  <div>
    <input type="text">
    <select name="select" id="select">
      <slot name="header" :items="items"></slot>
    </select>
  </div>
</template>

//v-slot
<script>
export default {
  name: 'Lesson8',
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
