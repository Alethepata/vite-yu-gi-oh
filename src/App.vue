<script>
import axios from 'axios';
import Header from './components/Header.vue';
import { store } from './data/store';
import Main from './components/Main.vue';
import Select from './components/Select.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Select
  },
  data() {
    return {
      store
    }
  },
  methods: {
    getApi() {
      axios.get(store.apiUrl, {
        params: {
          archetype:store.selectArchetype
        }
      })
        .then(res => {
          store.characterList = res.data.data

          store.characterList.forEach((character) => {
            if(character.archetype.includes(character.archetype)){
              if (!store.archetypeList.includes(character.archetype)) {
              store.archetypeList.push(character.archetype)
            }
          }
          })

      })
    }
  },
  mounted() {
    this.getApi()
  }
}

</script>

<template>

  <Header/>
  <Select @selected="getApi()"/>
  <Main/>

</template>



<style lang="scss">

@use './scss/main.scss'

</style>
