<template>
    <div class="card-element">
        <img :src="images" alt="">
        <p>{{title}}</p>
        <p>{{originalTitle}}</p>
        <p>{{lang}}</p>
        <p>{{vote}}</p>
    </div>
</template>

<script>
export default {
    props:["title","originalTitle","lang","vote"],
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