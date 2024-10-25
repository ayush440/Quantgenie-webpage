<script setup>
import { ref } from "vue";
import Sidebar from "primevue/sidebar";
import Button from "./Button.vue";

const visible = ref(false);

const scrollToSection = (sectionId) => {
  const element = document.getElementById(sectionId);
  if (element) {
    const yOffset = -60; // Adjust this value to fine-tune the scroll position
    const y = element.getBoundingClientRect().top + window.pageYOffset + yOffset;
    window.scrollTo({ top: y, behavior: 'smooth' });
  }
  visible.value = false; // Close sidebar if open
};

// Function to handle redirection to the app
const redirectToLoginSignup = () => {
  window.open("https://app.quantgenie.net/", "_blank");
};
</script>

<template>
  <nav class="text-white px-6 md:px-10 py-4 flex items-center justify-between 3xl:max-w-[85%] mx-auto sticky top-0 z-20 bg-[#1F242A] drop-shadow-md">
    <a href="/" class="w-[45%] md:w-[25%] xl:w-[12%]">
      <img src="/src/assets/images/loogoo.png" alt="Logo" class="w-[120px] max-h-[60px] object-contain" />

    </a>
    <div class="font-NeueMontreal-Light font-thin hidden xl:flex items-center gap-8 text-[16px] tracking-wider">
      <a @click.prevent="scrollToSection('hero')" href="#hero" class="cursor-pointer">Home</a>
      <a @click.prevent="scrollToSection('features2')" href="#features2" class="cursor-pointer">Features</a>
      <a @click.prevent="scrollToSection('why')" href="#why" class="cursor-pointer">Why</a>
      <a @click.prevent="scrollToSection('Pricing')" href="#Pricing" class="cursor-pointer">Pricing</a>
    </div>
    <!-- Login/Signup Button with @click redirect -->
    <Button class="hidden xl:block" @click="redirectToLoginSignup" title="Login/Signup" />
    
    <button class="xl:hidden" @click="visible = true">
      <i class="pi pi-bars text-[25px]"></i>
    </button>
    
    <Sidebar v-model:visible="visible" position="right">
      <div class="flex flex-col space-y-4 mt-8 text-[19px]">
        <p @click="scrollToSection('hero')">Home</p>
        <p @click="scrollToSection('features')">Features</p>
        <p @click="scrollToSection('why')">Strategy</p>
        <p @click="scrollToSection('about')">About Us</p>
        <p @click="scrollToSection('Pricing')">Pricing</p>
        <p @click="scrollToSection('contact')">Contact</p>
      </div>
      <!-- Sidebar Login/Signup button with link -->
      <a href="https://app.quantgenie.net/" target="_blank" class="mt-10">Login/Signup</a>
    </Sidebar>
  </nav>
</template>
