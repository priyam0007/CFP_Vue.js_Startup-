<template>
  <h1>{{ msg }}</h1>
<div id="app">
  <div class="row">
    <input v-model.number="num1" type="number" />
    <span>+</span>
    <input v-model.number="num2" type="number" />
    <span>=</span>
    <span>{{ num1 + num2 }}</span>
  </div>
  <div class="row second">
    <select v-model="name">
      <option>Carne Asada</option>
      <option>Pollo</option>
      <option>Bean</option>
      <option>Al Pastor</option>
    </select>
    <p v-if="name">My favorite kind of taco is {{ name }}</p>
  </div>
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
      num1: 0,
      num2: 0,
      name: ''
    }
  }
}
</script>
