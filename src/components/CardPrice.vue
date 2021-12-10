<template>
    <div class="card">
        <h3 class="title">{{ title }}</h3>
        <span class="category">{{ category }}</span>
        <span class="background_number">{{ price }}</span>
        <div class="price">
            <span>$</span>
            <span class="number">{{ price }}</span>
        </div>
        <span class="renewal">Per Mounth</span>
        <ul class="description">
            <li><strong>Creative</strong> Design Enable</li>
            <li><strong>Vibrant</strong> Color Usage</li>
            <li><strong>Eye</strong> Catching Design</li>
            <li><strong>Extreme</strong> Thipographyt</li>
            <li><strong>Exceptional</strong> Design</li>
        </ul>
        <button class="d-flex justify-content-between align-items-center button button_lg red_right_bottom">
            Order Now
            <i class="fas fa-long-arrow-alt-right"></i>
        </button>
    </div>
</template>

<script>
export default {
    name: 'CardPrice',
    props: {
        title: String,
        category: String,
        price: Number,
    }
}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';

.card {
    padding: 1rem 2.5rem;
    text-align: center;
    position: absolute;
    top: 0;
    border: 0;
    transform: translateY(-50%);
    border-radius: 20px;
    overflow: hidden;
    cursor: default;

    .background_number {
        position: absolute;
        left: 16%;
        bottom: 44%;
        font-size: 250px;
        font-weight: 600;
        opacity: 0.1;
    }

    .title {
        font-style: italic;
        font-size: 38px;
        font-weight: 600;
    }

    .category {

        text-transform: uppercase;
        font-size: 12px;
    }

    .price {
        display: flex;
        justify-content: center;

        .number {
            font-size: 90px;
            font-weight: 600;
            line-height: 110px;
        }
    }

    .renewal {
        font-size: 12px;
    }

    ul {
        list-style: none;
        padding: 1rem 0 0;
    }

    .button.red_right_bottom {
        box-shadow: 0px 0px 15px 5px rgba(247, 97, 107, 0.4);
    }

    &:hover {
        background: $red_to_right_bottom;
        color: #FFFFFF;
        box-shadow: 0px 0px 30px 0px #00000081;
    }

    &:hover .button.red_right_bottom {
        background: #FFFFFF;
        color: $primary_red;
        box-shadow: none;
    }
}

</style>