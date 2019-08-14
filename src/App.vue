<template>
  <div id="app">
    <h1>Basic Todo List</h1>
    <Display></Display>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
  import Display from './components/Display.vue';

export default {

  name: 'app',
  components: {
    Display
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
