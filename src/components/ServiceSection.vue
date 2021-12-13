<template>
  <section class="py-5" id="service-section">
    <div class="container">
        <div class="row">
            <!-- Header section -->
            <div class="col-12 text-center header_section">
                <span>Our Services</span>
                <p class="text"><strong>What</strong> We Do</p>
                <p>When, while the lovely valley teems with vapour aroung meand the</p>
            </div>
            <!-- Service Card -->
            <div class="col-3" v-for="(element, index) in ServiceList" :key="`element-${index}`">
                <CardService 
                    :image="element.image"
                    :title="element.title"
                    :text="element.text"
                />
            </div>
            <button class="button button_lg red_right_bottom">View All Service</button>
        </div>
    </div>
  </section>
</template>

<script>
import CardService from '@/components/CardService.vue'
export default {
    name: 'ServiceSection',
        components: {
        CardService,
    },
    data() {
        return {
            ServiceList: [
                {
                    image:require('@/assets/Group-247.png'),
                    title:'Data Analysis',
                    text:'When, while the lovely valley teems with vapour aroung meand the meridians sun strike the upper',
                },
                {
                    image:require('@/assets/Group-567.png'),
                    title:'SEO Optimization',
                    text:'When, while the lovely valley teems with vapour aroung meand the meridians sun strike the upper',
                },
                {
                    image:require('@/assets/Group-538.png'),
                    title:'Security Data',
                    text:'When, while the lovely valley teems with vapour aroung meand the meridians sun strike the upper',
                },
                {
                    image:require('@/assets/Group-566.png'),
                    title:'Branding Strategy',
                    text:'When, while the lovely valley teems with vapour aroung meand the meridians sun strike the upper',
                },
            ],
        }
    },
}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';

.header_section {
    padding-bottom: 6rem;
    span {
        color: $primary_red;
        font-size: $small;
    }
    .text {
        font-size: 34px;
    }
    p {
        font-size: $regular;
    }
}
button {
    margin: 80px auto;
}
</style>