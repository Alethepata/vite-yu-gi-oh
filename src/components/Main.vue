<script>
import CardsContainer from './partials/CardsContainer.vue';
export default {
    name: 'Main',
    components: {
        CardsContainer
    }
}
</script>

<template>
    <main>
        <CardsContainer/>
    </main>
</template>

<style lang="scss">
main{
    padding: 50px;
}
</style>