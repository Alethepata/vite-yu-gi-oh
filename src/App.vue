<script>
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
