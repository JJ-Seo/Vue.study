<template>
  <div>
    <form v-on:submit="subnitForm">
      <div>
        <label for="username">id: </label>
        <input type="text" id="username" v-model="username">
      </div>
      <div>
        <label for="password">pw: </label>
        <input type="password" id="password" v-model="password">
      </div>
      <button type="submit">Login</button>
    </form>

  </div>
</template>

<script>
export default {
  data: function() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    subnitForm: function(event){
      event.preventDefault();
      console.log(this.username, this.password);
    }
  }
}
</script>

<style>

</style>