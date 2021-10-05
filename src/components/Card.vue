<template>
    <div class="card-element">
        <img :src="img" alt="">
        <p>{{title}}</p>
    </div>
</template>

<script>
export default {
    props:["title"],
}
</script>

<style lang="scss" scoped>
.card-element{
    height: 250px;
    width:250px;
    background-color: rgb(54, 127, 196);
    margin:5px;

    flex-basis: calc(100% / 5 - 25px);
}
</style>