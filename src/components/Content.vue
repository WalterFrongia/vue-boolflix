<template>
    <div id="card-container">
        <div class="card-element" 
        v-for="(card, index) in listaFilm" :key="index">
        <ul>
            <li>{{card.title}}</li>
        </ul>
        </div>
    </div>
</template>

<script>
export default {
    name:"Content",
    props:["listaFilm"]

}
</script>

<style lang="scss" scoped>

</style>