<template>
 <div id="app">
  <h2>Tip Calculator</h2>
  <p><strong>Total: {{ customer1total }}</strong></p>
  <p>20%: {{ tip20 }}</p>
</div>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
     customer1total: 35.43    
    }
  },
  computed: {
    tip20() {
      return (this.customer1total*.2).toFixed(2)
    },
  }
}
</script>
