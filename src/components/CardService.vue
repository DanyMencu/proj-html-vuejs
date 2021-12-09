<template>
    <div href="#">
        <div class="service_card">
            <div class="img_card">
                <img :src="image" :alt="title">
            </div>
            <h4>{{ title }}</h4>
            <p>{{ text }}</p>
            <a href="#" class="arrow_icon red_right d-flex justify-content-center align-items-center">
                <i class="fas fa-arrow-right"></i>
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardService',
    props: {
        image: String,
        title: String,
        text: String,
    },

}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';

.service_card {
    position: relative;
    text-align: center;
    border-radius: 14px;
    padding: 120px 15px 10px;
    font-size: 14px;
    cursor: default;
    transition: all 0.4s;

    h4 {
        margin-top: 2rem;
    }

    .img_card {
        position: absolute;
        top: 0;
        left: 50%;
        transform: translate(-50%, -45%);
        width: 65%;
        background-color: #FFFFFF;
        margin: 0 auto;
        padding: 30px 10px;
        border-radius: 10px;
        transition: all 0.3s;

        img {
            width: 100%;
        }
    }

    &:hover {
        background: $blue_to_bottom;
        color: #FFFFFF;
    }

    &:hover .img_card {
        box-shadow: 0px 0px 10px 0px #BBBBBB;
    }

    .arrow_icon {
        position: absolute;
        top: 100%;
        left: 50%;
        width: 35px;
        height: 35px;
        transform: translate(-50%, -50%);
        text-decoration: none;
        font-size: 18px;
        border-radius: 50%;
        opacity: 0;
        transition: opacity 0.2s;
    }

    &:hover .arrow_icon {
        opacity: 1;
        color: #FFFFFF;
    }
}
</style>