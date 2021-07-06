<template>
    <div class="listrender">
        <h1>{{ msg }}</h1>

        <h2 v-for="name in names" :key="name">{{ name }}</h2>
        <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
        <h2 v-for="name in fullnames" :key="name.first">{{ name.first }} {{ name.last }}</h2>

        <div v-for="actor in actors" :key="actor.name">
            <h2>{{ actor.name }}</h2>
            <h3 v-for="movie in actor.movies" :key="movie"> {{ movie }}</h3>
        </div>

        <h2 v-for="value in myInfo" :key="value"> {{ value }} </h2>
        <h2 v-for="(value, key, index) in myInfo" :key="value"> {{ index }} {{ key }} {{ value }} </h2>

        <template v-for="name in names" :key="name">
            <h2> {{ name }}</h2>
            <hr>
        </template>

    </div>
</template>

<script>
export default {
  name: 'ListRendering',
  props: {
    msg: String
  },
  data() {
      return {
          names: ['Bruce', 'Clark', 'Diana'],
          fullnames: [
              {first: 'Bruce', last: 'Wayne'},
              {first: 'Clark', last: 'Kent'},
              {first: 'Princess', last: 'Diana'},
          ],
          actors: [
              {
                  name: "Cristian Bale",
                  movies: ['Batman', 'The prestige'],
              },
              {
                  name: 'Di Caprio',
                  movies: ['Titanic', 'Inception'],
              }
          ],
          myInfo: {
              name: 'Vishwas',
              channel: 'CodeEvolution',
              course: 'Vue 3',
          },
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