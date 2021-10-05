<template>
  <div id="app">
    <Header @search="loadMovies"/>,
    <Content :listaFilm="arrayMovies"/>,
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Content from './components/Content.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    Header,
    Content,
  },
  data: function(){
      return{
        //CREATO ARRAY PER SALVARE API
        arrayMovies:[],
      }
  },
  methods:{
    loadMovies: function(inputMessage){
      // console.log(inputMessage);
      if (inputMessage) {
          axios.get('https://api.themoviedb.org/3/search/movie',{
          params:{
            api_key:'a9f88cb578c09b30f91d0cd1be119282',
            query: inputMessage,
          }
        })
        .then ((response) => {
          console.log(response);
          //RICHIAMATO ARRAY CON THIS E ALL'INTERNO SALVATO API CON I DATI CHE CI INTERESSANO 
          this.arrayMovies = (response.data.results);
          console.log(this.arrayMovies);
        })
      }
    }
  },
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap';

</style>
