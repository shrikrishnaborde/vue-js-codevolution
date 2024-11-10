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
        isSoldOut: true,
        highlightColor: 'blue',
        headerSize : 50,
        headerStyleObject: {color: 'orange', 'font-size': '20px', padding: '20px'},
        baseStyleObject: { margin : '10px'}
      }
    }
  }
</script>

<template>
  <div>{{greet}} {{ name }}</div>
  <div v-html="channel"></div>
  <h2 :id="headingId">Heading</h2>
  <button :disabled="isDisabled">Button</button>
  <h2 class="underline" :class="className">Underlined text</h2>
  <h2 :class="isPromoted && 'promoted'">Promoted movie</h2>
  <h2 :class="isSoldOut ? 'soldOut': 'new'">Sold Out ?</h2>
  <h2 :class="['new','promoted']">Newly Promoted Movie</h2>
  <h2 :class="[isPromoted && 'promoted', isSoldOut ? 'soldOut': 'new']">Array conditional movie</h2>
  <h2 :class="{
    promoted: isPromoted,
    new: !isPromoted,
    soldOut: isSoldOut
  }">Object conditional movies</h2>

  <h2 v-bind:style="{color: highlightColor, 'font-size': headerSize + 'px', padding: '20px'}">Inline Style</h2>
  <h2 v-bind:style="headerStyleObject">Inline Style with data</h2>
  <h2 v-bind:style="[headerStyleObject,baseStyleObject]">Multiple styles object</h2>
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


