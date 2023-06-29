<script setup>

</script>

<template>
  <main class="subscribe my-24 flex items-center justify-center">
    <div class="py-12 px-4 min-h-350 w-full flex flex-wrap items-center justify-center rounded-lg shadow-custom-shadow">
      <div class="w-full text-center mt-4">
        <h1 class="oswald uppercase text-4xl mb-3 mt-0">get update from anywhere</h1>
        <p class="text-custom-btn-gray mb-12">Be the first to get latest update on new products up for sale</p>
      </div>

      <div class="w-600 mt-4 mb-12 h-14 flex flex-wrap gap-y-2 items-center justify-center gap-x-8">
        <input class="border border-slate-300 w-350 h-full rounded-full pl-5" type="email" name="email" id="email" placeholder="Enter your email" required>
        <button class="capitalize text-white w-200 border border-custom-blue rounded-full h-full px-4 bg-custom-blue">subscibe now</button>
      </div>
    </div>
  </main>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@500&display=swap');
  
  main {
    padding: 0px 10%;
  }
  .oswald {
    font-family: "Oswald";
    text-underline-offset: 17px;
    text-decoration-thickness: 2px;
  }
</style>