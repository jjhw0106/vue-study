<template>
  <!-- submit이후 화면이 새로고침 되는 것을 막기위해 .prevent 붙인다. -->
  <form v-on:submit.prevent ="submitForm">
    <div>
      <label for="username">id: </label>
      <input id="username" type="text" v-model="username">
    </div>
    <div>
      <label for="password">password: </label>
      <input id="password" type="password" v-model="password">
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
import axios from 'axios';

export default {
  data: function() {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    submitForm: function() {
      console.log(this.username, this.password);
      var url = 'https://jsonplaceholder.typicode.com/posts';
      var data = {
        username: this.username,
        password: this.password,
      }
      axios
        .post(url, data)
        .then(function(response) {
          console.log(response);
        })
        .catch(function(error) {
          console.log(error);
        });
    }
  }
}
</script>

<style>

</style>