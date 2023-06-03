<script setup>

</script>

<template>
  <main class="subscribe mb-8 mt-24 flex items-center justify-center">
    <div class="py-12 min-h-350 w-full flex flex-col items-center justify-center rounded-lg shadow-custom-shadow">
      <h1 class="oswald uppercase text-4xl mb-3 mt-8">get update from anywhere</h1>
      <p class="text-custom-btn-gray mb-12">Be the first to get latest update on new products up for sale</p>

      <div class="w-600 flex items-center justify-center gap-x-8 mx-auto my-4 h-14">
        <input class="border border-slate-300 w-full h-full rounded-full pl-5" type="email" name="email" id="email" placeholder="Enter your email" required>
        <button class="capitalize text-white w-52 border border-custom-blue rounded-full h-full px-4 bg-custom-blue">subscibe now</button>
      </div>
    </div>
  </main>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@500&display=swap');
  
  main {
    padding: 0px 5%;
  }
  .oswald {
    font-family: "Oswald";
    text-underline-offset: 17px;
    text-decoration-thickness: 2px;
  }
</style>