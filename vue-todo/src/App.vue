<template>
  <div id="app">
    <div class="container">
      <div class="com-md-6 offser-md-3">
        <h1 class="text-center mb-4">Todo App</h1>
        <input type="text" class="form-control" v-model="userInput">
      </div>
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
