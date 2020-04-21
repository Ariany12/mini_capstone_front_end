<template>
  <div class="Products-Index">
    <h1>{{ message }}</h1>
    <h1>{{ products }}</h1>
  </div>
</template>

<style>
</style>

<script>
import axios  from "axios"
export default {
  data: function() {
    return {
      message: "Welcome to Vue.js!",
      products: []
    };
  },
  created: function() {
    axios.get('/api/products').then(response => {
      console.log(response.data)
    })
  },
  methods: {}
};
</script>