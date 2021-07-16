<template>

  <div>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <BindingText msg="VUE JS 3 Tutorial: 1-4" /> -->
    <!-- <Rendering msg="VUE JS 3 Tutorial: 10-12Conditional Rendering" /> -->
    <!-- <ListRendering msg="VUE JS 3 Tutorial: 13-14 List Rendering" /> -->
    <Methods msg="VUE JS 3 Tutorial: 16 Methods" />
    <Events msg="VUE JS 3 Tutorial: 17 Event Handling" />

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import BindingText from './components/1_4_BindingText.vue'
// import Rendering from './components/ConditionalRendering.vue'
// import ListRendering from './components/ListRendering.vue'
import Methods from './components/16_Methods.vue'
import Events from './components/17_EventHandling.vue'

export default {
  name: 'App',
  
  components: {
    // BindingText,
    // Rendering,
    // ListRendering,
    // HelloWorld,
    Methods,
    Events,
  },

  data() {
    return {
  
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

.underline {
  text-decoration: underline;
}

 .promoted {
   font-style: italic;
   color: orange;
 }

 .new {
   color: olivedrab
 }

 .sold-out {
   color: red; 
 }

</style>
