<template>
  <section>
      <div class="container">
            <div class="row justify-content-around align-items-center">
                <div class="col-12 text-center header_section">
                    <span>Price List</span>
                    <p class="text"><strong>Our</strong> Pricing</p>
                    <p>When, while the lovely valley teems with vapour aroung meand the upper surface</p>
                </div>
                <!-- Price card -->
                <div
                    class="col-3 card_container"
                    v-for="(element, index) in PriceList" :key="`element-${index}`"
                >
                    <CardPrice
                        :title="element.title"
                        :category="element.category"
                        :price="element.price"
                    />
                </div>
            </div>
      </div>
  </section>
</template>

<script>
import CardPrice from '@/components/CardPrice.vue'

export default {
    name: 'PriceSection',
    components: {
        CardPrice,
    },
    data() {
        return {
            PriceList: [
                {
                    title:'Designing',
                    category:'process',
                    price:40,
                },
                {
                    title:'Developing',
                    category:'product',
                    price:60,
                },
                {
                    title:'Supporting',
                    category:'clients',
                    price:80,
                },
            ]
        }
    },
}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';

section {
    background: $blue_to_right;
    padding: 1.5rem 0 2rem;

    .header_section {
        height: 60vh;
        color: #FFFFFF;

        span {
            color: #B6246E;
            font-size: 12px;
        }

        .text {
                font-size: 34px;
        }

        p {
            font-size: 14px;
        }
    }
}

.card_container {
    position: relative;
}


</style>