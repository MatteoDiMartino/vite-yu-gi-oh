<script>
    import { store } from '../store.js';
    import Cardlist from './Cardlist.vue';
    import SelectCom from './SelectCom.vue'


    export default {
        name: 'AppMain',
        components: {
            Cardlist,
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
                <div class="ms-h d-flex justify-content-center bg-white">
                    <div class="w-100 px-4 pt-4 pb-0">
                        <div class="bg-black text-white px-3 py-2">
                            ciao
                        </div>
                    </div>
                    <Cardlist v-for="mscard in store.cards" :key="mscard.id" :cardInfo="mscard" class="pt-0 mt-0"></Cardlist>
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