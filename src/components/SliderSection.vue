<template>
    <section class="py-5" id="portfolio-section">
        <!-- Header Section -->
        <div class="container">
            <div class="row justify-content-between align-items-center">
                <div class="col-2">
                    <span>Portfolio</span>
                    <p><strong>Lastest</strong> work</p>
                </div>
                <div class="col-2 d-flex justify-content-end align-items-center">
                    <a href="#" class="arrow_icon d-flex justify-content-center align-items-center">
                        <i class="fas fa-arrow-left"></i>
                    </a>
                    <a href="#" class="arrow_icon d-flex justify-content-center align-items-center ms-3">
                        <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
            </div>
        </div>
        <!-- Project portfolio SLIDER -->
        <div class="card_container">
            <CardPortfolio
                v-for="(element, index) in Portfolio" :key="`element-${index}`"
                :image="element.image"
                :title="element.title"
                :text="element.text"
            />
        </div>
        <!-- Dot counter slide -->
        <div class="d-flex justify-content-center align-items-center pt-5">
            <i
                v-for="(element, index) in Portfolio" :key="`Dot-${index}`"
                class="fas fa-circle dot px-1"
            ></i>
        </div>
    </section>
</template>

<script>
import CardPortfolio from '@/components/CardPortfolio.vue'

export default {
    name: 'SliderSection',
    components: {
        CardPortfolio,
    },
    data() {
        return {
            Portfolio: [
                {
                    image:require('@/assets/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg'),
                    title:'Purinky Products',
                    text:'Digital Experience',
                },
                {
                    image:require('@/assets/8wa60okr-1-790x576.jpg'),
                    title:'Basket of Flower on table',
                    text:'Branding Strategy',
                },
                {
                    image:require('@/assets/DRY-1-790x576.jpg'),
                    title:'Purinky Products',
                    text:'Digital Experience',
                },
                {
                    image:require('@/assets/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg'),
                    title:'Satisfy Poster',
                    text:'Branding Strategy',
                },
                {
                    image:require('@/assets/84316050-0af0-49db-a53a-241d47ddad0e-2-790x576.jpg'),
                    title:'Mock-up Interview',
                    text:'Digital Experience',
                },
            ]
        }
    }

}

</script>

<style scoped lang="scss">
@import '@/styles/Variables';
section {
    background: #02023011;

    .dot {
        font-size: 8px;
        color: $gray;

        &:first-child {
            color: $primary_red;
        }
    }
    }

.container {
    padding: 3rem 0;

    span {
        color: $primary_red;
        font-size: $small;
    }

    p {
        font-size: 28px;
        line-height: 20px;
    }

    .arrow_icon {
        color: $primary_red;
        border: 1px solid $primary_red;
    }
}

.card_container {
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    font-size: $regular;
}

</style>