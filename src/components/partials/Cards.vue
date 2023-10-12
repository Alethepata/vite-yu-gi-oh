<script>
export default {
    name: 'Cards',
    props: {
        name: String,
        archetype: String,
        cardImg:Object
    }
}
</script>

<template>

<div class="col mb-5">

    <div class="card text-center border-0 ">
        <div class="image">
        <img
        v-for="img in cardImg"
        :key="img.id"
        :src="img.image_url" 
        alt="">
    </div>
    <div class="text">
        <h3>{{ name }}</h3>
        <p>{{ archetype }}</p>        
    </div>
    </div>


</div>
  
</template>

<style lang="scss" scoped>

@use '../../scss/partials/var' as *;

.card{
    width: 230px;
    height: 500px;
    background-color: $orange;
    img{
    width: 100%;
    height: 100%;
    }
}


</style>