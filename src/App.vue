<script>
  import axios from 'axios';
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
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response) => {
          store.card = response.data.data;
          console.log(store.card)
        })
      }
    },
    mounted() {
      this.getCardFromApi();
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
