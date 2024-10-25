<script setup>
import Button from '../components/Button.vue';
</script>

<template>
  <section class="px-6 md:px-10 py-10  flex flex-col xl:flex-row items-center justify-between 3xl:max-w-[85%] mx-auto space-y-6">
  <div class="w-full xl:w-[50%] space-y-6">
      <h1 class="font-Inter text-[40px] leading-[55px] md:leading-[65px] md:text-[50px]"><span class="text-custom-blue">Transform Your Trading with QuantGenie's</span> All-in-One SaaS Platform</h1>
      <p class="font-Inter font-thin tracking-wide text-[17px] md:text-[19px]">QuantGenie offers a seamless, scalable, and powerful SaaS solution for traders who want to automate and optimize their stock, options, and commodities trading. Access our cloud-based platform from anywhere, anytime, and elevate your trading with cutting-edge algorithms and advanced manual trading tools.</p>
      <Button title="Get Started"/>
  </div>
  <div class="w-full xl:w-[45%]">
    <img src="../assets/images/heroBg.webp" alt="" class="w-full md:w-[80%] mx-auto xl:m-0 xl:w-full ">
  </div>
  </section>
</template>
