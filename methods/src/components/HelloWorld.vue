<template>
  <h1>{{ msg }}</h1>
  <div id="app" >
  <div @mousemove="xCoordinate" :style="{ backgroundColor: `hsl(${x}, 80%, 50%)` }" class="box">
    <p>
      <button @click="increment">+</button> 
      {{ counter }} 
      <button @click="decrement">-</button>
    </p>
    <p>Pixels across: {{ x }}</p>
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
   counter: 0,
      x: 0
  	}
  },
  methods: {
	  increment() {
	  	this.counter++;
	  },
    decrement() {
	  	this.counter--;
	  },
    xCoordinate(e) {
      this.x = e.clientX;
    }
  }
}
</script>
<style>
#app {
  width: 200vw;
  height: 200vh;
  padding: 15vmin;
  font-size: 30px;
  transition: 0.2s background-color ease;
}
.box {
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  padding: 10vmin;
}
</style>