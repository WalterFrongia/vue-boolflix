<template>
    <div id="card-container">
        <card v-for="(card, index) in listaFilm" :key="index" :title="card.title"/>
    </div>
</template>

<script>
import Card from './Card.vue'

export default {
    name:"Content",
    props:["listaFilm"],
    components: {
        Card,
    },

}
</script>

<style lang="scss" scoped>

#card-container{
    display: flex;
    flex-wrap: wrap;

    margin:auto;
    width:80%;
}
</style>