<template>
  <h1>{{ msg }}</h1>
  <h2>{{Message}} to Hello World</h2>
  <p>{{message2}}</p>
  <div id = "app">{{Message1}} Nice to meet vue</div>
  <button @click="count++">count is: {{ count }}</button>
  <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      count: 0,
      Message: 'Welcome',
      Message1: 'Do your Best',
      message2: 'Vue.js'
    }
  }
}
</script>
