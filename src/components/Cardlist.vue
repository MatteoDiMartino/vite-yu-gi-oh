<script>

export default {
        name: 'Cardlist',
        props: {
            cardInfo: Object
        }
    }

</script>

<template>

<div class="d-flex ms-card-container">
    <div class="my-3 ms-bg-infocard">
        <img :src="cardInfo.card_images[0].image_url_small" alt="img" class="ms-w-card">
        <div class="text-center py-2">
            <h3>{{ cardInfo.name }}</h3>
            <span>{{ cardInfo.archetype }}</span>
        </div>
    </div>    
</div>


</template>

<style scoped lang="scss">

.ms-w-card {
    width: 100%;
}

.ms-card-container {
    flex-wrap: wrap;
    width: 15%;
    height: 15%;

    .ms-bg-infocard {
        background-color: #D48F38;

    }
}
</style>