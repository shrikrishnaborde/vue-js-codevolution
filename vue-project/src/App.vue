<script>

  export default {
    name : "App",
    data(){
      return{
        name: "Batman",
        greet: "Hello",
        channel: "<b>codeevoluation</b>",
        headingId:"heading",
        isDisabled: true,
        className: 'danger'
      }
    }
  }
</script>

<template>
  <div>{{greet}} {{ name }}</div>
  <div v-html="channel"></div>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Button</button>
  <h2 class="underline" v-bind:class="className">Underlined text</h2>
</template>

<style>

.underline {
  text-decoration: underline;
}

</style>


