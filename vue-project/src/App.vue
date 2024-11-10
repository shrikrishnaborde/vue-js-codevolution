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
        className: 'danger',
        isPromoted: true,
        isSoldOut: true
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
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted movie</h2>
  <h2 v-bind:class="isSoldOut ? 'soldOut': 'new'">Sold Out ?</h2>
  <h2 v-bind:class="['new','promoted']">Newly Promoted Movie</h2>
  <h2 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'soldOut': 'new']">Array conditional movie</h2>
</template>

<style>

.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.soldOut {
  color: red;
}

.new {
  color: green;
}

</style>


