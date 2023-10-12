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

    <img
    v-for="img in cardImg"
    :key="img.id"
    :src="img.image_url" 
    alt="">

    <h1>{{ name }}</h1>

    <p>{{ archetype }}</p>
  
</template>

<style>

</style>