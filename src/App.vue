<script>
import axios from 'axios';
import Header from './components/Header.vue';
import { store } from './data/store';
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data() {
    return {
      store
    }
  },
  methods: {
    getApi() {
      axios.get(store.apiUrl)
        .then(res => {
          store.characterList = res.data.data
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
  <Main/>

</template>



<style lang="scss">

@use './scss/main.scss'

</style>
