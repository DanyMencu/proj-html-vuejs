<template>
    <div class="card">
        <div class="img_card">
            <img :src="image" :alt="title">
        </div>
        <div class="d-flex justify-content-between align-items-center h-100 px-2">
            <span class="title"><strong>{{ title }}</strong></span>
            <span class="text">{{ text }}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardPortfolio',
    props: {
        image: String,
        title: String,
        text: String,
    },
}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';

.card {
    width: calc(100% / 4);
    height: 45vh;
    flex-shrink: 0;
    overflow: hidden;
    cursor: pointer;
    margin: 0 10px;
    border: 0;
    border-radius: 10px;

    .img_card {
        height: 80%;
        
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 10px;
        }
    }

    &:hover {
        background: $red_to_right;
    }

    &:hover .title {
        transform: scale(1.05);
        color: $white;
    }

    &:hover .text {
        transform: scale(0.8);
        color: #ffffff77;
    }
}

</style>