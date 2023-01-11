<template>
  <div id="app">

    
    <h1>My bookshelf</h1>
    <div class="search-wrapper">
    <input type="text" v-model="search" v-on:input="search"/>
    <Shelf/>
    </div>
  </div>
</template>

<script>

import Shelf from './components/Shelf';


export default {
  name: 'App',
  components: {
    Shelf
  }
}


</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
