<script setup>
  import { ref, reactive } from 'vue';
  import { RouterLink } from 'vue-router';
  import logo from '../assets/images/logo.webp';

  const showShopCategory = ref(false);
  const showBlogCategory = ref(false);
  const showPagesCategory = ref(false);
  const shopCategory = [
    {name: "Shop Category", path: "category.html"},
    {name: "Product Details", path: "single-product.html"},
    {name: "Product Checkout", path: "checkout.html"},
    {name: "Confirmation", path: "confirmation.html"},
    {name: "Shopping Cart", path: "cart.html"},
  ]
  const blogCategory = [
    {name: "Blog", path: "blog.html"},
    {name: "Blog Details", path: "single-blog.html"},
  ]
  const pagesCategory = [
    {name: "Login", path: "login.html"},
    {name: "Register", path: "register.html"},
    {name: "Tracking", path: "tracking-order.html"},
  ]
  const login = ref(false);
  const cart = reactive([
    {name: "cart one"},
    {name: "cart two"}
  ])

</script>

<template>
  <nav class="flex items-center justify-between">
    <a class="w-32" href="index.html"><img :src="logo" alt="Logo"></a>
    <div class="text-black flex items-center justify-center" id="navbarSupportedContent">
      <ul class="flex items-start justify-between w-full gap-x-10">
        <li class="hover:text-custom-blue"><a class="" href="index.html">Home</a></li>
        <li class="" @mouseenter="showShopCategory = true" @mouseleave="showShopCategory = false">
          <a href="#" class="hover:text-custom-blue">Shop</a>
          <ul v-if="showShopCategory" class="absolute z-10 left-0 w-250 top-7 bg-white">
            <li v-for="shop in shopCategory" class="px-4 py-4 hover:bg-custom-blue hover:text-white transition-all duration-300"><a class="" :href="shop.path">{{ shop.name }}</a></li>
          </ul>
        </li>
        <li class="" @mouseenter="showBlogCategory = true" @mouseleave="showBlogCategory = false">
          <a href="#" class="hover:text-custom-blue">Blog</a>
          <ul class="absolute z-10 left-0 w-250 top-7 bg-white" v-if="showBlogCategory">
            <li v-for="blog in blogCategory" class="px-4 py-4 hover:bg-custom-blue hover:text-white transition-all duration-300"><a class="" :href="blog.path">{{ blog.name }}</a></li>
          </ul>
        </li>
        <li class="" @mouseenter="showPagesCategory = true" @mouseleave="showPagesCategory = false">
          <a href="#" class="hover:text-custom-blue">Pages</a>
          <ul class="absolute z-10 left-0 w-250 top-7 bg-white" v-if="showPagesCategory">
            <li v-for="page in pagesCategory" class="px-4 py-4 hover:bg-custom-blue hover:text-white transition-all duration-300"><a class="" :href="page.path">{{ page.name }}</a></li>
          </ul>
        </li>
        <li class="hover:text-custom-blue"><a class="" href="contact.html">Contact</a></li>
      </ul>
    </div>

    <div class="flex items-center justify-center">
      <ul class="flex items-center justify-center gap-x-4">
        <li class=""><button><img class="icon" src="https://img.icons8.com/ios/50/null/search--v1.png" alt="search"></button></li>
        <li class="cart relative"><button><img class="icon" src="https://img.icons8.com/material-outlined/24/null/shopping-cart--v1.png" alt="shopping-cart"><span class="text-white text-xs rounded-full bg-custom-blue absolute top-0">{{ cart.length }}</span></button> </li>
      </ul>
    </div>

    <button class="border border-gray-100 hover:border-blue-500 rounded-3xl transition-all duration-500 px-8 py-2"> Buy Now </button>
  </nav>
</template>

<style scoped>
  nav {
    height: 90px;
    padding: 10px 5%;
  }
  .icon {
    width: 15px;
  }
  .cart span {
    padding: 0px 5px;
    top: -13px;
    left: 10px;
  }
</style>