<template>
    <section id="blog-section">
        <div class="container">
          <!-- Header section -->
            <div class="row justify-content-center align-items-center">
                <div class="col-6 text-center header_section">
                    <span>Blog</span>
                    <p class="text"><strong>Latest</strong> Posts</p>
                    <p>When, while the lovely valley teems with vapour aroung meand the upper surface .</p>
                </div>
            </div>
                <!-- Posts area -->
            <div class="row justify-content-between align-items-stretch">
                <CardPost
                        v-for="(element, index) in Posts" :key="`post-${index}`"
                        :image='element.image'
                        :title='element.title'
                        :text='element.text'
                        :author='element.author'
                        :date='element.date'
                        :index='index'
                />
            </div>
        </div>
    </section>
</template>

<script>
import CardPost from '@/components/CardPost.vue'
export default {
    name: 'Blog',
    components: {
        CardPost,
    },
    data() {
        return {
            Posts: [
                {
                    image: require('@/assets/headway-537308-unsplash-1380x703.jpg'),
                    title:'Amazon gets CCI nod to acquire 49% stake in',
                    text:'When, while the lovely valley teems with vapor around me, and the maridian sun s ...',
                    author:'Paul',
                    date:'April 21, 2019',
                },
                {
                    image: require('@/assets/studio-republic-644339-unsplash-1380x703.jpg'),
                    title:'Clearing Corporations get SEBI nod to invest in overnight funds',
                    text:'When, while the lovely valley teems with vapor around me, and the maridian sun s ...',
                    author:'Paul',
                    date:'April 21, 2019',
                },
                {
                    image: require('@/assets/timon-studler-63413-unsplash-1380x703.jpg'),
                    title:'Shabnam Dillion, wife of RSSB chief Gurinder Dhillon, passes away in London',
                    text:'When, while the lovely valley teems with vapor around me, and the maridian sun s ...',
                    author:'Paul',
                    date:'April 21, 2019',
                },
            ]
        }
    },
}
</script>

<style scoped lang="scss">
@import '@/styles/Variables';
section {
    padding: 16rem 0 6rem;
    .header_section {
        padding-bottom: 2rem;
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
    .col-3 {
        display: flex;
    }
}
</style>