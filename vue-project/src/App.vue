<script>

  export default {
    name : "App",
    data(){
      return{
        name: "Batman",
        greet: "Hello",
        channel: "codeevoluation"
      }
    }
  }
</script>

<template>
  <div>{{greet}} {{ name }}</div>
  <div v-text="channel"></div>
</template>

<style scoped>


</style>
