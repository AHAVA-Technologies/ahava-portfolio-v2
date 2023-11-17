<script lang="ts" setup>
import { Carousel, Slide, Navigation } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";
</script>
<template>
  <div
    id="hero"
    class="w-full relative overflow-hidden !min-h-[80vh] animate-slide pt-32 grid items-center h-full grid-cols-1 col md:grid-cols-5"
  >
    <div
      class="flex items-center justify-start w-full col-span-1 md:col-span-3"
    >
      <div class="space-y-10">
        <div class="text-black">
          <h3
            class="text-xl font-semibold animate-slideInDown text-primary-600"
          >
            CREATIVE & INNOVATIVE
          </h3>
          <h1
            class="font-light animate-zoomIn max-w-[50ch] md:text-left text-justify mt-5 text-gray-600"
          >
            Our mission is to develop cutting-edge software solutions that
            streamline and optimize business processes for organizations across
            various industries.
          </h1>
        </div>
        <div class="mt-5 font-semibold">
          <nuxt-link
            class="px-8 py-3 text-white rounded-sm bg-primary-600 hover:bg-primary-800"
            to="/"
            >Free Quote</nuxt-link
          >
          <nuxt-link
            class="px-8 py-3 ml-5 border rounded-sm text-primary-600 border-primary-600 hover:bg-primary-50"
            to="/"
            >Contact Us</nuxt-link
          >
        </div>
      </div>
    </div>
    <div class="w-full col-span-1 md:col-span-2">
      <client-only>
        <Vue3Lottie
          animationLink="/animation/lottie-hero.json"
          class="w-full"
        />
      </client-only>
      <!-- <nuxt-img src="/animation/hero.svg" alt="Hero" class="h-full object-" /> -->
    </div>
  </div>
</template>

<style>
.carousel__prev,
.carousel__next,
.carousel__prev--active,
.carousel__next--active {
  @apply text-white border border-white rounded-full w-12 bg-midnight-950 bg-opacity-50 h-12 hover:text-white hover:bg-opacity-80;
}
.carousel__icon {
  @apply w-32;
}
.carousel__prev--disabled,
.carousel__next--disabled {
  display: none;
}
</style>
