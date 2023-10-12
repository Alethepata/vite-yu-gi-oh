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
@use '../scss/partials/var' as *;
main{
    background-color: $orange;
    padding: 50px;
}
</style>