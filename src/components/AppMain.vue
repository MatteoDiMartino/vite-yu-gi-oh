<script>
    import Cardlist from './Cardlist.vue';


    export default {
        name: 'AppMain',
        components: {
            Cardlist
        }
    }
</script>

<template>
    <main class="ms-main-bg">
        <div class="container">
            <div class="row">
                <div class="ms-h">
                    <Cardlist></Cardlist>
                </div>
            </div>
        </div>
    </main>
</template>

<style scoped lang="scss">

.ms-main-bg {
    background-color: #D48F38;

    .ms-h {
        height: 88.9vh;
    }
}

</style>