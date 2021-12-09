<template>
  <section class="py-5">
    <div class="container">
        <div class="row">
            <div class="col-12 text-center header_section">
                <span>Our Services</span>
                <p class="text"><strong>What</strong> We Do</p>
                <p>When, while the lovely valley teems with vapour aroung meand the</p>
            </div>
            <div class="col-3" v-for="(element, index) in ServiceList" :key="`element-${index}`">
                <CardService 
                    :image="element.image"
                    :title="element.title"
                    :text="element.text"
                />
            </div>
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
.header_section {
    padding-bottom: 6rem;

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

a {
    text-decoration: none;
    color: #000000;
}
</style>