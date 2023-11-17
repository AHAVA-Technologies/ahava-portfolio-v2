<script lang="ts" setup>
defineProps({
  customClass: {
    type: String,
    required: false,
  },
});
</script>
<template>
  <nav
    class="absolute right-0 z-50 flex flex-col w-full text-lg font-semibold bg-white top-14 h-fit gap-y-5"
  >
    <nuxt-link
      exact-active-class="relative text-primary-600 after:absolute after:w-full after:h-[2px] after:border-t-primary-600 after:border-t-[2px] after:bottom-0 after:left-0"
      class="relative flex items-center justify-center h-full hover:text-primary-600 hover:after:absolute hover:after:w-full hover:after:h-[2px] hover:after:border-t-primary-600 after:transition-all after:duration-500 hover:after:border-t-[2px] hover:after:bottom-0 after:left-0"
      to="#hero"
      >Home</nuxt-link
    >
    <nuxt-link
      exact-active-class="relative text-primary-600 after:absolute after:w-full after:h-[2px] after:border-t-primary-600 after:border-t-[2px] after:bottom-0 after:left-0"
      class="relative flex items-center justify-center h-full hover:text-primary-600 hover:after:absolute hover:after:w-full hover:after:h-[2px] hover:after:border-t-primary-600 after:transition-all after:duration-500 hover:after:border-t-[2px] hover:after:bottom-0 after:left-0"
      to="#about"
      >About</nuxt-link
    >
    <nuxt-link
      exact-active-class="relative text-primary-600 after:absolute after:w-full after:h-[2px] after:border-t-primary-600 after:border-t-[2px] after:bottom-0 after:left-0"
      class="relative flex items-center justify-center h-full hover:text-primary-600 hover:after:absolute hover:after:w-full hover:after:h-[2px] hover:after:border-t-primary-600 after:transition-all after:duration-500 hover:after:border-t-[2px] hover:after:bottom-0 after:left-0"
      to="#services"
      >Services</nuxt-link
    >
    <nuxt-link
      class="relative flex items-center justify-center h-full hover:text-primary-600 hover:after:absolute hover:after:w-full hover:after:h-[2px] hover:after:border-t-primary-600 after:transition-all after:duration-500 hover:after:border-t-[2px] hover:after:bottom-0 after:left-0"
      to="#request-quote"
      >Contact</nuxt-link
    >
  </nav>
</template>
