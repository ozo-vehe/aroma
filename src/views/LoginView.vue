<script setup>
  import { RouterLink } from 'vue-router';

</script>

<template>
  <main>
    <div class="header bg-custom-background flex flex-col justify-center h-400">
      <h1 class="oswald w-full text-center text-5xl mb-2">Login</h1>
      <div class="links m-0 w-full text-center">
        <RouterLink to="/">Home</RouterLink> - <RouterLink to="/login">Login</RouterLink>
      </div>
    </div>

    <div class="form flex items-center justify-center flex-wrap py-24">
      <div class="registerContainer box-border px-12 flex gap-4 items-center justify-center flex-col bg-custom-blue text-white h-600 w-500">
        <h2 class="text-2xl oswald">New to our website?</h2>
        <p class="text-center text-sm mb-4">
          There are advances being made in science and technology everyday,
          an a good exampple of this is the
        </p>
        
        <RouterLink to="/register" class="border border-gray-100 hover:bg-custom-gray hover:text-custom-blue rounded-3xl transition-all duration-500 px-12 py-2">
          Create an Account
        </RouterLink>
      </div>

      <form class="shadow-lg h-600 w-500 py-8 flex gap-4 flex-col items-center justify-center">
        <h2 class="text-center oswald text-2xl uppercase mb-8">Log in to Enter</h2>
        <div class="username border-b-2 w-2/3 py-2 px-4 mb-4">
          <input class="outline-none w-full border-none" type="text" placeholder="Username" required>
        </div>

        <div class="password border-b-2 w-2/3 py-2 px-4 mb-4">
          <input class="outline-none w-full border-none" type="password" placeholder="Password" required>
        </div>

        <div class="flex gap-4 items-center justify-start w-2/3 mb-4">
          <input class="outline-none border-none" type="checkbox">
          <span class="text-custom-btn-gray text-sm">Keep me logged in</span>
        </div>

        <div class="formBtb w-2/3 mb-2">
          <button class="border border-custom-blue hover:border-custom-blue bg-custom-blue hover:bg-white text-white hover:text-custom-blue w-full rounded-3xl transition-all duration-500 px-8 py-2"> Log In </button>
        </div>

        <p class="cursor-pointer w-2/3 text-center text-sm text-custom-blue">Forgot Password?</p>
      </form>
    </div>
  </main>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@500&display=swap');
 
  .oswald {
    font-family: "Oswald";
  }
  .form {
    padding-left: 10%;
    padding-right: 10%;
  }
</style>