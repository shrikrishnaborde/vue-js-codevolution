<script>

  export default {
    name : "App",
    data(){
      return{
        name: "Batman",
        greet: "Hello",
        channel: "<b>codeevoluation</b>"
      }
    }
  }
</script>

<template>
  <div>{{greet}} {{ name }}</div>
  <div v-html="channel"></div>
</template>

<style scoped>


</style>
