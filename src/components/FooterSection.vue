<script setup>
  const links = ["Home", "Shop", "Blog", "Product", "Brand", "Contact"];
  const footerImages = [
    { name: "image 1", src: "" },
    { name: "image 2", src: "" },
    { name: "image 3", src: "" },
    { name: "image 4", src: "" },
    { name: "image 5", src: "" },
    { name: "image 6", src: "" },
  ]
</script>

<template>
  <main>
    <div>
      <h1>Our Mission</h1>
      <p>
        At Aroma, our mission is to revolutionize the way people 
        shop by providing a seamless and enjoyable online shopping 
        experience. We strive to be the go-to destination for customers 
        seeking convenience, quality, and variety in their purchases.
      </p>
    </div>

    <div>
      <div class="quickLinks">
        <h2>Quick Links</h2>
        <ul>
          <li v-for="link in links">{{ link }}</li>
        </ul>
      </div>

      <div class="footerGallery">
        <img v-for="image in footerImages" :src="image.src" :alt="image.name">
      </div>

      <div class="footerContactUs">
        <div class="headOffice">
          <i>Icon</i>
          <div class="details">
            <h3>Head Office</h3>
            <p>123, Main Street, Kaduna</p>
          </div>
        </div>

        <div class="phoneNumber">
          <i>Icon</i>
          <div class="details">
            <h3>Phone Number</h3>
            <p>+234 123 456 789 0</p>
            <p>+234 123 456 789 0</p>
            <p>+234 123 456 789 0</p>
          </div>
        </div>

        <div class="email">
          <i>Icon</i>
          <div class="details">
            <h3>Email</h3>
            <p>aroma@website.com</p>
            <p>aromahq@website.com</p>
          </div>
        </div>
      </div>
    </div>

    <div class="footerText">
      <p>Copyright ©2023 All rights reserved | This template is made with love by Colorlib</p>
    </div>
  </main>
</template>

<style scoped>
</style>