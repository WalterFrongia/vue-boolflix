<template>
  <div id="app">
    <Header @search="loadMovies"/>,
    <Main/>,
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
  },
  methods:{
    loadMovies: function(inputMessage){
      console.log(inputMessage);
      
    }
  },
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap';

</style>
