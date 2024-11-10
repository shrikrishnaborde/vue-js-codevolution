<script>

  export default {
    name : "App",
    data(){
      return{
        name: "Batman",
        greet: "Hello",
        channel: "<b>codeevoluation</b>",
        headingId:"heading",
        isDisabled: true
      }
    }
  }
</script>

<template>
  <div>{{greet}} {{ name }}</div>
  <div v-html="channel"></div>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Button</button>
</template>

