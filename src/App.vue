<template>
  <div>
    <div>Hello {{ name }}</div>
    <div v-html="channel"></div>
    <h2 :id="headingId">Heading</h2>
    <button :disabled="isDisabled">Bind</button>
    <h2 class="underline">Underlined Text</h2>
    <h2 class="underline" :class="status">Status</h2>
    <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
    <h2 :class="isSoldout ? 'sold-out' : 'new'">Soldout? Movie</h2>
    <h2 :class="['new', 'promoted']">Newly Promoted Movie</h2>
    <h2 :class="[isPromoted && 'promoted', isSoldout ? 'sold-out' : 'new']">Array Condition Movie</h2> 
    <h2 :class="{
      promoted: isPromoted,
      new: !isSoldout,
      'sold-out': isSoldout,
      }">Object Conditional Movie</h2>
      <h2 :style="{
        color: highlightColor,
        'font-size': headerSize + 'px',
        fontSize: headerSize + 'px',
        padding: '20px',
      }">Inline Style</h2>
      <h2 :style="headerStyleObject">Style Object</h2>
      <div :style="[baseStyleObject, successStyleObject]">Success Style</div>
      <div :style="[baseStyleObject, dangerStyleObject]">Danger Style</div>
  
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Rendering msg="Conditional Rendering" />
    <ListRendering msg="List Rendering" />

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Rendering from './components/ConditionalRendering.vue'
import ListRendering from './components/ListRendering.vue'

export default {
  name: 'App',
  
  components: {
    Rendering,
    ListRendering,
    // HelloWorld,
  },

  data() {
    return {
      name: "Batman",
      channel: "<strong>Codevolution</strong>",
      headingId: "heading",
      isDisabled: true,
      status: "danger",
      isPromoted: true,
      isSoldout: true,
      highlightColor: "orange",
      headerSize: 50,
      headerStyleObject: {
        color: "orange",
        fontSize: "50px",
        padding: "20px"
      },
      baseStyleObject: {
        fontSize: "50px",
        padding: "10px",
      },
      successStyleObject: {
        color: "green",
        backgroundColor: "lightgreen",
        border: "1px solid green",
      },
      dangerStyleObject: {
        color: "darkred",
        backgroundColor: "red",
        border: "1px solid dardred",
      },
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
