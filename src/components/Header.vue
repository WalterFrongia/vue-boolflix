<template>
    <div id="header-section" class="ps-5 pt-5">
        <img src="" alt="">
        <input v-model = "message" placeholder="search">
        <button @click="$emit('search',message)">search</button>
    </div>
</template>

<script>
export default {
    name:"Header",
    data: function(){
        return{
            message:"",
        }
    }

}
</script>

<style lang="scss" scoped>

</style>