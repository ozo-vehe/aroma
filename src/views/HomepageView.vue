<script setup>
  // Components
  import HeroSection from '../components/HeroSection.vue';
  import ProductsSection from '../components/ProductsSection.vue';
  import BestSellerSection from '../components/BestSellersSection.vue';
  import SubscribeSection from '../components/SubscribeSection.vue';

  // Local files
  import shoe from '../assets/images/hero-slide1.png.webp';
  import headphone from '../assets/images/hero-slide2.png.webp';
  import cubes from '../assets/images/hero-slide3.png.webp';

  // Variables
  const products = [
    {image: shoe, name: "sneakers", category: "accessory item"},
    {image: headphone, name: "wireless headphone", category: "accessory item"},
    {image: cubes, name: "cubes", category: "accessory item"},
  ]
</script>

<template>
  <main class="">
    <HeroSection />
    <section class="flex gap-x-4 mt-4">
      <div class="group overflow-hidden relative w-100%" v-for="(product, index) in products" :key="index">
        <img :src="product.image" :alt="product.name">
        <div class="absolute top-0 z-10 bg-white/80 w-full h-full translate-y-8 opacity-0 group-hover:translate-y-0 group-hover:opacity-100 transition-all duration-500">
          <div class="pl-4 pr-20 py-4 bg-custom-blue text-white capitalize absolute bottom-12 left-0 z-10">
            <h3 class="oswald text-2xl mb-1">{{ product.name }}</h3>
            <p class="text-sm">{{ product.category }}</p>
          </div>
        </div>
      </div>
    </section>
    <ProductsSection/>
    <BestSellerSection class="relative"/>
    <SubscribeSection/>
  </main>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200&display=swap');
  .oswald {
    font-family: "Oswald";
    font-weight: 600;
  }
</style>
