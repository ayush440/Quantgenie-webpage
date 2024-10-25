<script setup>
import Button from '../components/Button.vue';
</script>

<template>
    <section class="px-6 md:px-10 py-10 xl:py-20 font-Inter 3xl:max-w-[85%] mx-auto">
        <div class="text-center space-y-3">
            <h1 class="text-[40px] xl:text-[44px]">Flexible SaaS <span class="text-custom-blue">Pricing & Free Trial</span></h1>
            <p class=" font-thin tracking-wide mx-auto w-[90%] xl:w-[70%] text-[16px]">QuantGenie offers flexible, subscription-based Pricing so you only pay for what you need. Whether you're a beginner or a seasoned trader, our tiered plans ensure you get access to the tools and features that best suit your trading style.</p>
        </div>
        <div class="grid grid-cols-1 xl:grid-cols-2 gap-8 mt-10 xl:mt-20 2xl:px-10">
            <div class="p-8 card rounded-3xl space-y-6">
                <h3 class="text-custom-blue text-[44px]">7-Day Free Trial</h3>
                <p class="font-thin text-[19px]">Explore QuantGenie risk-free and unlock the full potential of automated and manual trading for 7 days.</p>
                <Button title="Get Started"/>
            </div>
            <div class="p-8 card rounded-3xl space-y-6">
                <h3 class="text-custom-blue text-[44px]">Affordable Monthly Pricing</h3>
                <p class="font-thin text-[19px]">Get premium features with a transparent, subscription-based model.</p>
                <Button title="Get Started"/>
                <p>240+ people Subscribed in last 24 hours</p>
            </div>
        </div>
    </section>
</template>

<style scoped>
.card {
  box-shadow: -5px -5px 15px rgba(255, 255, 255, 0.1),
    /* top-left white shadow */ 10px 10px 20px rgba(0, 0, 0, 0.7); /* bottom-right black shadow */
}
</style>

