<script setup>
  // Components
  import Product from './Product.vue';

  // Assests
  import watch from '../assets/images/product1.png.webp';
  import freshwash from '../assets/images/product2.png.webp';
  import flashlight from '../assets/images/product3.png.webp';
  import bottle from '../assets/images/product4.png.webp';
  import bag from '../assets/images/product5.png.webp';
  import car from '../assets/images/product6.png.webp';
  import speaker from '../assets/images/product7.png.webp';
  import chargingCar from '../assets/images/product8.png.webp';
   
  // Variables/Data
  const products = [
    {
      name: "quartz belt watch",
      image: watch,
      category: "accessories",
      price: 150,
      availability: true,
      quantity: 10,
      details: "Mill Oil is an innovative oil filled radiator with the most modern technology. If you are looking for something that can make your interior look awesome, and at the same time give you the pleasant warm feeling during the winter.",
    },
    {
      name: "women freshwash",
      image: freshwash,
      category: "beauty",
      price: 150,
      availability: true,
      quantity: 10,
      details: "Mill Oil is an innovative oil filled radiator with the most modern technology. If you are looking for something that can make your interior look awesome, and at the same time give you the pleasant warm feeling during the winter.",
    },
    {
      name: "room flash light",
      image: flashlight,
      category: "decor",
      price: 150,
      availability: true,
      quantity: 10,
      details: "Mill Oil is an innovative oil filled radiator with the most modern technology. If you are looking for something that can make your interior look awesome, and at the same time give you the pleasant warm feeling during the winter.",
    },
    {
      name: "bottle",
      image: bottle,
      category: "accessories",
      price: 150,
      availability: true,
      quantity: 10,
      details: "Mill Oil is an innovative oil filled radiator with the most modern technology. If you are looking for something that can make your interior look awesome, and at the same time give you the pleasant warm feeling during the winter.",
    },
    {
      name: "man office bag",
      image: bag,
      category: "accessories",
      price: 150,
      availability: true,
      quantity: 10,
      details: "Mill Oil is an innovative oil filled radiator with the most modern technology. If you are looking for something that can make your interior look awesome, and at the same time give you the pleasant warm feeling during the winter.",
    },
    {
      name: "charging car",
      image: car,
      category: "kids toy",
      price: 150,
      availability: true,
      quantity: 10,
      details: "Mill Oil is an innovative oil filled radiator with the most modern technology. If you are looking for something that can make your interior look awesome, and at the same time give you the pleasant warm feeling during the winter.",
    },
    {
      name: "bluetooth speaker",
      image: speaker,
      category: "accessories",
      price: 150,
      availability: true,
      quantity: 10,
      details: "Mill Oil is an innovative oil filled radiator with the most modern technology. If you are looking for something that can make your interior look awesome, and at the same time give you the pleasant warm feeling during the winter.",
    },
    {
      name: "charging car",
      image: chargingCar,
      category: "kids toy",
      price: 150,
      availability: true,
      quantity: 10,
      details: "Mill Oil is an innovative oil filled radiator with the most modern technology. If you are looking for something that can make your interior look awesome, and at the same time give you the pleasant warm feeling during the winter.",
    },
  ]
</script>

<template>
  <main class="mb-8 mt-24">
    <p class="text-sm text-custom-btn-gray mb-1">Popular item in the market</p>
    <h1 class="oswald text-5xl mb-12">Trending <span class="oswald underline decoration-custom-blue">Product</span></h1>
    <div class="border border-red-300 flex flex-wrap gap-4 justify-center items-start">
      <Product v-for="(product, index) in products" :key="index" :product="product"/>
    </div>
  </main>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200&display=swap');
  
  main {
    padding: 0px 5%;  
  }
  .oswald {
    font-family: "Oswald";
    font-weight: 600;
    text-underline-offset: 17px;
    text-decoration-thickness: 2px;
  }
</style>