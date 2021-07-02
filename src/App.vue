<template>
  <div>
    <div>Hello {{ name }}</div>
    <div v-html="channel"></div>
    <h2 v-bind:id="headingId">Heading</h2>
    <button v-bind:disabled="isDisabled">Bind</button>
    <h2 class="underline">Underlined Text</h2>
    <h2 class="underline" v-bind:class="status">Status</h2>
    <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
    <h2 v-bind:class="isSoldout ? 'sold-out' : 'new'">Soldout? Movie</h2>
    <h2 v-bind:class="['new', 'promoted']">Newly Promoted Movie</h2>
    <h2 v-bind:class="[isPromoted && 'promoted', isSoldout ? 'sold-out' : 'new']">Array Condition Movie</h2> 
    <h2 v-bind:class="{
      promoted: isPromoted,
      new: !isSoldout,
      'sold-out': isSoldout,
      }">Object Conditional Movie</h2>
      <h2 v-bind:style="{
        color: highlightColor,
        'font-size': headerSize + 'px',
        fontSize: headerSize + 'px',
        padding: '20px',
      }">Inline Style</h2>
      <h2 v-bind:style="headerStyleObject">Style Object</h2>
      <div v-bind:style="[baseStyleObject, successStyleObject]">Success Style</div>
      <div v-bind:style="[baseStyleObject, dangerStyleObject]">Danger Style</div>
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
