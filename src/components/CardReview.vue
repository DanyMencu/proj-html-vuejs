<template>
<div class="col-4 ">
    <div class="review">
    <div class="img_profile">
        <img :src="image" :alt="author">
    </div>
    <div class="rating">
        <i class="fas fa-star"
            v-for="(n, index) in rating" :key="`Voto pieno n-${index}`"
        ></i>
        <i class="far fa-star"
            v-for="(n, index) in (5 - rating)" :key="`Voto vuoto n-${index}`"
        ></i>
    </div>
    <p class="text">
        {{ text }}
    </p>
    <span class="author">
        {{ author }}
    </span>
    <span class="role">
        {{ role }}
    </span>
    </div>
</div>
</template>

<script>
export default {
    name: 'CardReview',
    props: {
        image: String,
        rating: Number,
        text: String,
        author: String,
        role: String,
    },

}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';

.review {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    .img_profile {
        width: 80px;
        height: 80px;
        border: 3px solid $primary_red;
        border-radius: 50%;
        overflow: hidden;

        img {
            width: 100%;
            object-fit: cover;
        }
    }

    .rating {
        color: $primary_red;
        padding: 2rem 0;
    }

    .text {
        text-align: center;
    }

    .author {
        font-weight: 600;
        padding: 1rem 0 0.5rem;
    }
}

</style>