<template>
    <section>
        <div class="container">
          <!-- Header section -->
            <div class="row justify-content-center align-items-center">
                <div class="col-6 text-center header_section">
                    <span>Testimonial</span>
                    <p class="text"><strong>What</strong> People Say</p>
                    <p>When, while the lovely valley teems with vapour aroung meand the upper surface .</p>
                </div>
            </div>

          <!-- Review section -->
            <div class="row justify-content-center align-items-center reviews">
                <!-- Card -->
                <CardReview
                v-for="(element, index) in Reviews" :key="`Review-${index}`"
                :image="element.image"
                :rating="element.rating"
                :text="element.text"
                :author="element.author"
                :role="element.role"
                />
            </div>

          <!-- Partner section -->
            <div class="col d-flex justify-content-around partners">
                <div
                    class="row justify-content-around align-items-center"
                    v-for="(element, index) in PartnersList" :key="`Partner n-${index}`"
                >
                    <a href="#">
                    <img :src="element.image" :alt="element.name">
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import CardReview from '@/components/CardReview.vue'

export default {
    name: 'ReviewsSection',
    components: {
        CardReview,
    },
    data() {
        return {
            Reviews: [
                {
                    image: require('@/assets/szabo-viktor-1266895-unsplash-1024x1024.png'),
                    rating: 3,
                    text: 'When, while the lovely valley teems with vapor around me, and the maridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.',
                    author: 'Michkel Anegl',
                    role: 'Marketing Management',
                },
                {
                    image: require('@/assets/philipe-cavalcante-539505-unsplash-1024x1024.png'),
                    rating: 4,
                    text: 'When, while the lovely valley teems with vapor around me, and the maridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.',
                    author: 'Michkel Anegl',
                    role: 'Marketing Management',
                },
                {
                    image: require('@/assets/fabio-spinelli-695744-unsplash-1024x1024.png'),
                    rating: 1,
                    text: 'When, while the lovely valley teems with vapor around me, and the maridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.',
                    author: 'Michkel Anegl',
                    role: 'Marketing Management',
                },
            ],
            PartnersList: [
                {
                    image: require('@/assets/client-1-1.png'),
                    name: 'Golden nedloG',
                },
                {
                    image: require('@/assets/clienty-2.png'),
                    name: 'Sweety Cafeteria',
                },
                {
                    image: require('@/assets/clienty-4.png'),
                    name: 'Fastlane Sportwear',
                },
                {
                    image: require('@/assets/client-5.png'),
                    name: 'Mighty Forniture',
                },
                {
                    image: require('@/assets/clienty-3.png'),
                    name: 'Jack Roller',
                },
            ],
        }
    },

}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';

section {
    padding: 1rem 0 5rem;

    .header_section {
        padding-bottom: 2rem;

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

    .reviews {
        padding: 0.5rem 0 3rem;
    }

    .partners {
        padding: 4rem 0 6rem;
    }
}

</style>