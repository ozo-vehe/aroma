<script setup>
  // Importing images
  import image1 from '../assets/images/footer1.webp'
  import image2 from '../assets/images/footer2.webp'
  import image3 from '../assets/images/footer3.webp'
  import image4 from '../assets/images/footer4.webp'
  import image5 from '../assets/images/footer5.webp'
  import image6 from '../assets/images/footer6.webp'

  // Variables
  const links = ["Home", "Shop", "Blog", "Product", "Brand", "Contact"];
  const footerImages = [
    { name: "image 1", src: image1 },
    { name: "image 2", src: image2 },
    { name: "image 3", src: image3 },
    { name: "image 4", src: image4 },
    { name: "image 5", src: image5 },
    { name: "image 6", src: image6 },
  ]
</script>

<template>
  <main class="bg-custom-dark-blue text-slate-200 flex flex-wrap items-start justify-center gap-8">
    <div class="w-300">
      <h1 class="oswald text-3xl mb-4">Our Mission</h1>
      <p class="text-sm text-custom-btn-gray">
        At Aroma, our mission is to revolutionize the way people 
        shop by providing a seamless and enjoyable online shopping 
        experience. We strive to be the go-to destination for customers 
        seeking convenience, quality, and variety in their purchases.
      </p>
    </div>

    <div class="min-w-500 flex flex-wrap items-start justify-between gap-8">
      <div class="quickLinks w-250">
        <h2 class="oswald text-2xl mb-4">Quick Links</h2>
        <ul class="text-sm text-custom-btn-gray">
          <li v-for="link in links">{{ link }}</li>
        </ul>
      </div>

      <div class="footerGallery w-250">
        <h2 class="oswald text-2xl mb-4">Gallery</h2>
        <div class="flex w-200 flex-wrap gap-4">
          <img v-for="image in footerImages" :src="image.src" :alt="image.name">
        </div>
      </div>

      <div class="footerContactUs w-250">
        <h2 class="oswald text-2xl mb-4">Contact Us</h2>

        <div class="headOffice mb-6 flex flex-wrap items-start gap-4 text-sm">
          <div class="p-2 rounded-full bg-custom-blue h-8 w-8 relative">
            <img class="rotate-90 absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2" width="24" height="24" src="https://img.icons8.com/external-tanah-basah-glyph-tanah-basah/48/ffffff/external-send-user-interface-tanah-basah-glyph-tanah-basah.png" alt="external-send-user-interface-tanah-basah-glyph-tanah-basah"/>
          </div>
          <div class="details">
            <h3 class="mb-2">Head Office</h3>
            <p class="text-custom-btn-gray">123, Main Street, Kaduna</p>
          </div>
        </div>

        <div class="phoneNumber mb-6 text-sm flex flex-wrap gap-4">
          <div class="p-2 rounded-full bg-custom-blue h-8 w-8 relative">
            <img class="-rotate-90 absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2" width="24" height="24" src="https://img.icons8.com/ios-filled/50/ffffff/phone.png" alt="phone"/>
          </div>
          <div class="details">
            <h3 class="mb-2">Phone Number</h3>
            <p class="text-custom-btn-gray">+234 123 456 789 0</p>
            <p class="text-custom-btn-gray">+234 123 456 789 0</p>
            <p class="text-custom-btn-gray">+234 123 456 789 0</p>
          </div>
        </div>

        <div class="email text-sm flex flex-wrap gap-4">
          <div class="p-2 rounded-full bg-custom-blue h-8 w-8 relative">
            <img class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2" width="20" height="20" src="https://img.icons8.com/ios-filled/50/ffffff/mail.png" alt="mail"/>
          </div>
          <div class="details">
            <h3 class="mb-2">Email</h3>
            <p class="text-custom-btn-gray">aroma@website.com</p>
            <p class="text-custom-btn-gray">aromahq@website.com</p>
          </div>
        </div>
      </div>
    </div>

    <div class="footerText text-center bg-custom-dark-blue-shade">
      <p>Copyright ©2023 All rights reserved | This design was gotten from <a class="text-custom-blue underline underline-offset-2" href="https://preview.colorlib.com/">Colorlib</a></p>
    </div>
  </main>
</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@200&display=swap');
  
  main {
    padding: 50px 5% 0px;
  }
  .oswald {
    font-family: "Oswald";
  }
  .footerText {
    width: 100vw;
    margin: 0px -5.4%;
    padding: 30px;
  }
</style>