<template>
  <h1>{{ msg }}</h1>
  <div id="app">
  <ul>
    <li v-for="num in 5" :key="num">
      {{ num }}
    </li>
  </ul>
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
      count: 0
    }
  }
}
</script>
