<template>
    <a href="#">
        <div class="service_card">
            <div class="img_card">
                <img :src="image" :alt="title">
            </div>
            <h4>{{ title }}</h4>
            <p>{{ text }}</p>
        </div>
    </a>
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
.service_card {
    position: relative;
    text-align: center;
    border-radius: 14px;
    padding: 120px 15px 10px;
    font-size: 14px;
    transition: all 0.4s;

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
        background-color: #040839;
        color: #FFFFFF;
    }

    &:hover .img_card {
        box-shadow: 0px 0px 10px 0px #BBBBBB;
    }
}
</style>