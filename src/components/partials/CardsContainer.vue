<script>
import { store } from '../../data/store';
import Cards from './Cards.vue';
export default {
    name: 'CardsContainer',
    components: {
        Cards
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>

    <cards
    v-for="card in store.characterList"
    :key="card.id"
    :name="card.name"
    :archetype="card.archetype"
    :cardImg="card.card_images"
    />
  
</template>

<style>

</style>