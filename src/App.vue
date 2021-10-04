<template>
  <div id="app">
    <Header @search="loadMovies"/>,
    <Main/>,
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    Header,
    Main,
  },
  methods:{
    loadMovies: function(inputMessage){
      console.log(inputMessage);
      axios.get('https://api.themoviedb.org/3/search/movie?api_key=a9f88cb578c09b30f91d0cd1be119282&query=parola')
      .then(function (response) {
        console.log(response);
      })
    }
  },
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap';

</style>
