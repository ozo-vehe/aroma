<script setup>
  import MazPhoneNumberInput from 'maz-ui/components/MazPhoneNumberInput';
</script>

<template>
  <main class="flex relative flex-wrap justify-center gap-14 my-4 before:absolute before:top-0 before:leeft-0 before:bg-custom-gray before:w-full before:h-1/2">
          <MazPhoneNumberInput
            v-model="phoneNumber"
            show-code-on-list
            color="primary"
            placeholder="000 000 000 000"
            no-example
          />
  </main>
</template>

<style scoped>
  main {
    padding: 50px 10%;
  }
</style>