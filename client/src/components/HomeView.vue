<template>

    <div class="flex flex-col min-h-screen font-Roboto bg-gray-baft">   
    <HeadBanner />
    <TopShop />
    <MidTop />
    <MidSection />
    <MidBottom />
    <TailShop />
    <Footer />
    </div>
    
</template>

<script setup>

  import HeadBanner from './components/HeadBanner.vue';
  import TopShop from './components/TopShop.vue';
  import MidTop from './components/MidTop.vue';
  import MidSection from './components/MidSection.vue';
  import MidBottom from './components/MidBottom.vue';
  import TailShop from './components/TailShop.vue';
  import Footer from "./components/Footer.vue";

</script>

<style lang="scss" scoped>

</style>