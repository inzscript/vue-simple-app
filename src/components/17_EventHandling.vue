<template>
    <div class="container">
        <h1>{{ msg }}</h1>
        


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