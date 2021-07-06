<template>
    <div class="render">
        <h1>{{ msg }}</h1>
        <h2 v-if="num === 0">The number is zero</h2>
        <h2 v-else-if="num < 0">The number is negative</h2>
        <h2 v-else-if="num > 0">The number is positive</h2>
        <h2 v-else>NOT a number</h2>
        <template v-if="display">
            <h2>Vishwas</h2>
            <h2>CodeEvolution</h2>
            <h2>Vue</h2>
        </template>

        <h2 v-show="showElement">Using v-show</h2>
        <h2 v-if="showElement">Using v-if</h2>
    </div>
</template>

<script>
export default {
  name: 'Rendering',
  props: {
    msg: String
  },
  data() {
      return {
          num: "Hi",
          display: true,
          showElement: false,
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>