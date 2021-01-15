<template>
  <div>
  <p>hello</p>
  </div>
</template>

<script>


export default {
  name: 'App',
  data (){
    return { 
      pokemon: []
  }
  },
  components: {
  },
  mounted(){
    fetch('https://pokeapi.co/api/v2/pokemon?limit=151')
    .then(res => res.json())
    .then(pokemon => this.pokemon = pokemon);
  }
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
