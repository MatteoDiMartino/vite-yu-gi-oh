<script>
    import { store } from '../store.js';
    import Cardlist from './Cardlist.vue';


    export default {
        name: 'AppMain',
        components: {
            Cardlist
        },
        data () {
            return {
                store
            };
        }
    }
</script>

<template>
    <main class="ms-main-bg">
        <div class="container">
                <div class="bg-black text-white px-3 py-3"></div>
                <div class="ms-h d-flex justify-content-center bg-white">
                    <Cardlist v-for="mscard in store.cards" :key="mscard.id" :cardInfo="mscard" class="mt-4"></Cardlist>
                </div>
        </div>
    </main>
</template>

<style scoped lang="scss">

.ms-main-bg {
    background-color: #D48F38;
    .ms-h {
        height: 100%;
        flex-wrap: wrap;
    }
}

</style>