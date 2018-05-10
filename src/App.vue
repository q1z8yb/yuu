<template>
  <div id="app">
      <input type="text" v-model = "message" @keyup.enter = "handleAdd">
      <ul>
        <li v-for="item of list">
          {{item}}
        </li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      message :'',
      list :[]
    }
  },
  methods :{
    handleAdd(e) {
        this.list.push(e.target.value)
    }
  }
}
</script>

<style>

</style>
