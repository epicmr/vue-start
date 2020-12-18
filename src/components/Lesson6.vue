<template>
  <div>
    <div>
      <span style="white-space: pre-line;">{{message}}</span>
    </div>
    <textarea type="text" v-model="message"></textarea>
    <div>
      <input type="checkbox" v-model="checked">
      <label for="apple">{{checked}}</label>
    </div>
    <div>
      <input type="checkbox" id="capple" value="apple" v-model="checkedarr">
      <label for="apple">apple</label>

      <input type="checkbox" id="coringe" value="oringe" v-model="checkedarr">
      <label for="oringe">oringe</label>

      <input type="checkbox" id="cbanana" value="banana" v-model="checkedarr">
      <label for="banana">banana</label>

      <div>
        <span>checked: {{checkedarr}}</span>
      </div>
    </div>
    <div>
      <input type="radio" id="papple" value="apple" v-model="picked">
      <label for="apple">apple</label>

      <input type="radio" id="poringe" value="oringe" v-model="picked">
      <label for="oringe">oringe</label>

      <input type="radio" id="pbanana" value="banana" v-model="picked">
      <label for="banana">banana</label>

      <div>
        <span>picked: {{picked}}</span>
      </div>
      <div>
        <select v-model="selected" multiple>
          <option value="A">A</option>
          <option value="B">B</option>
          <option value="C">C</option>
        </select>
        <br />
        <span>selected: {{selected}}</span>
      </div>
      <div>
        <select v-model="selected1" multiple>
          <option :key="data" v-for="data in checkedarr">{{data}}</option>
        </select>
        <br />
        <span>selected: {{selected1}}</span>
      </div>
    </div>
  </div>
</template>

//v-model
<script>
export default {
  name: 'Lesson1',
  data () {
    return {
      message: "",
      checked: true,
      checkedarr: ["apple", "oringe", "banana"],
      picked: "",
      selected: "",
      selected1: ""
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
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
