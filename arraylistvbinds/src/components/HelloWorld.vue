<template>
  <h1>{{ msg }}</h1>
 <div id="app">
  <h3>What is your favorite kind of taco?</h3>
  <textarea v-model="tacos"></textarea>
  <br>
  <button :class="[tacos ? activeClass : '']">Let us know!</button>
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
      tacos: '',
      activeClass: 'active'
    }
  }
 }
</script>
