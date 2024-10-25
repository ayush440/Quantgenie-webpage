<script setup>
const feat = [
  {
    title: "Stocks",
    desc: "Access individual stocks for detailed analysis and automated trading",
    img: "/stock.svg",
  },
  {
    title: "Stock & Index Options",
    desc: "Trade Nifty, Bank Nifty, Finnifty, and other major indices.",
    img: "/pointer.svg",
  },
  {
    title: "Commodities",
    desc: "Automate and trade major commodities like Crude Oil and Natural Gas.",
    img: "/Petrol.svg",
  },
];
</script>

<template>
  <section
    class="font-Inter p-6 md:p-10 xl:py-28 2xl:py-40  bg-custom-blue relative"
  >
  <div class="3xl:max-w-[85%] mx-auto">
  <div class="absolute bottom-0 right-0 hidden xl:block">
    <img src="/bg.svg" alt="">
  </div>
    <div class="flex flex-col items-center justify-center space-y-4">
      <h1
        class="font-light text-center leading-[50px] text-[35px] md:text-[44px] w-[80%] xl:w-[40%] mx-auto"
      >
        Comprehensive Market Coverage
      </h1>
      <p class="font-light text-center text-[19px]">
        QuantGenie provides support across major asset classes, including:
      </p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-3 mt-20 px-10 xl:px-20 gap-8">
      <div v-for="item in feat" class="flex flex-col items-center space-y-4">
        <div class="card p-5 rounded-3xl">
          <img :src="item.img" alt="" />
        </div>
        <div class="space-y-2">
          <p class="text-center font-bold text-[17px] xl:text-[19px]">{{ item.title }}</p>
          <p class="text-center text-[16px] mx-auto w-full xl:w-[80%]">{{ item.desc }}</p>
        </div>
      </div>
    </div>
</div>
  </section>
</template>

<style scoped>
.card {
  box-shadow: -5px -5px 15px rgba(255, 255, 255, 0.5),
 10px 10px 20px rgba(0, 0, 0, 0.3); /* bottom-right black shadow */
}
</style>
