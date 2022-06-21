<template>
  <h1>{{ msg }}</h1>
 <div id="app">
  <h3>What is your favorite kind of taco?</h3>
  <textarea v-model="tacos"></textarea>
  <br>
  <button v-show="tacos" type="submit">Let us know!</button>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      tacos: ''
    }
   }
 }
</script>
