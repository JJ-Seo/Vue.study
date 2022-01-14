<template>
  <div id="app">
    <div class="container">
      <h1 class="text-center">Todo App</h1>
      <input type="text" class="form-control" v-model="userInput">

    </div>
  </div>
</template>

<script>

export default {
  name: 'App',

  data() {
    return{
      userInput:''
    };
  },
  components: {
    
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
