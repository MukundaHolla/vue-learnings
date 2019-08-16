<template>
  <div id="app">
    <h1>{{ msg }}</h1>
    <Navbar />
    <Blogs />
  </div>
</template>

<script>
import Navbar from "./Navbar";
import Blogs from './Blogs';

export default {
  name: 'app',
  components: {
    Navbar,
    Blogs
  },
  data () {
    return {
      msg: 'Welcome to Mukundas Vue.js App'
    }
  },
  methods: {
    
  }
}
</script>

<style>
h1 {
  font-weight: normal;
  text-align: center;
}
</style>
