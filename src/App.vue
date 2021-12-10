<template>
  <div id="app">
      <Header />

      <main>
        <Hero />

        <ServiceSection />

        <ProjectSection />

        <SliderSection />

        <PriceSection />

        <Blog />

        <ReviewsSection />
      </main>

      <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Hero from './components/Hero.vue';
import ServiceSection from './components/ServiceSection.vue';
import ProjectSection from './components/ProjectSection.vue';
import SliderSection from './components/SliderSection.vue';
import PriceSection from './components/PriceSection.vue';
import Blog from './components/Blog.vue';
import ReviewsSection from './components/ReviewsSection.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    ServiceSection,
    ProjectSection,
    SliderSection,
    PriceSection,
    Blog,
    ReviewsSection,
    Footer,
  }
}
</script>

<style lang="scss">
@import '@/styles/Globals';
@import '@/styles/Utilities';

</style>
