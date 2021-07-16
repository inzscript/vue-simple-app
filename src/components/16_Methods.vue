<template>
    <div class="container">
        <h1>{{ msg }}</h1>
        <p>{{ 2 + 3 + 8 }}</p>
        <p>Call Method - Add: {{ add( 10, 20, 5) }} </p>
        <p>Call Method - Multiply: {{ multiply(5) }} </p>


    </div>
</template>

<script>
export default {
  name: 'Methods',
  props: {
    msg: String
  },
  data() {
      return {
          baseMultiplier: 5,     
      }
  },
  methods: {
    add(a, b, c) {
      return a + b + c
    },
    multiply(num) {
      return num * this.baseMultiplier
    },
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>