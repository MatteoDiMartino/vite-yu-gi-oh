<script>
  import { store } from './store.js';
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';


  export default {
    components: {
      AppHeader,
      AppMain
    },
    data () {
      return {
        store
      };
    },
    methods: {
      getCardFromApi() {
        
      }
    }
  }
</script>

<template>

<AppHeader></AppHeader>
<AppMain></AppMain>

</template>

<style scoped lang="scss">
 @use './style/generic.scss'
</style>
