<template>
    <div class="card-element">
        <p>{{title}}</p>
        <p>{{originalTitle}}</p>
        <img v-if="lang == 'it' " src="../assets/images/italian_flag.png" alt="">
        <img v-else-if="lang == 'en' " src="../assets/images/english_flag.png" alt="">
        <p v-else>{{lang}}</p>
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
    img{
        width: 10%;
    }
}
</style>