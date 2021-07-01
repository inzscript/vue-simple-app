<template>
  <div>
    <div>Hello {{ name }}</div>
    <div v-html="channel"></div>
    <h2 v-bind:id="headingId">Heading</h2>
    <button v-bind:disabled="isDisabled">Bind</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: "Batman",
      channel: "<strong>Codevolution</strong>",
      headingId: "heading",
      isDisabled: true,
    };
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
