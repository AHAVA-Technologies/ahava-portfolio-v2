<script lang="ts" setup>
const hashedRoute = useRoute().hash;
const showDropDownNav = ref(false);

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});

const isScrolling = ref(false);
const handleScroll = () => {
  const header = document.querySelector("header");
  const scrollY = window.scrollY;
  if (scrollY > 10) {
    isScrolling.value = true;
  } else {
    isScrolling.value = false;
  }
};
</script>
<template>
  <header
    class="fixed top-0 left-0 z-50 flex items-center w-full px-5 transition-all duration-300 md:px-20 backdrop-filter backdrop-blur-lg bg-opacity-60"
    :class="
      isScrolling
        ? ' top-0 text-black md:py-2 py-3 md:h-24 h-12 shadow'
        : 'bg-transparent sm:text-black md:h-28 h-14 py-3 md:py-0'
    "
  >
    <div class="relative flex items-center justify-between w-full h-full">
      <div class="flex items-center gap-x-5">
        <img
          src="/img/ahava-logo.png"
          class="md:w-[180px] md:h-[100px] h-[50px] object-contain"
          alt="Ahava Digital Solutions Logo"
        />
      </div>
      <nav class="hidden h-full text-lg font-semibold gap-x-5 md:flex">
        <nuxt-link
          :class="
            hashedRoute === ''
              ? 'relative text-primary-600 after:absolute after:w-full after:h-[2px] after:border-t-primary-600 after:border-t-[2px] after:bottom-0 after:left-0'
              : ''
          "
          class="relative flex items-center justify-center h-full hover:text-primary-600 hover:after:absolute hover:after:w-full hover:after:h-[2px] hover:after:border-t-primary-600 after:transition-all after:duration-100 hover:after:border-t-[2px] hover:after:bottom-0 after:left-0"
          href="#hero"
          >Home</nuxt-link
        >
        <nuxt-link
          :class="
            hashedRoute === '#about'
              ? 'relative text-primary-600 after:absolute after:w-full after:h-[2px] after:border-t-primary-600 after:border-t-[2px] after:bottom-0 after:left-0'
              : ''
          "
          class="relative flex items-center justify-center h-full hover:text-primary-600 hover:after:absolute hover:after:w-full hover:after:h-[2px] hover:after:border-t-primary-600 after:transition-all after:duration-100 hover:after:border-t-[2px] hover:after:bottom-0 after:left-0"
          href="#about"
          >About</nuxt-link
        >
        <nuxt-link
          :class="
            hashedRoute === '#service'
              ? 'relative text-primary-600 after:absolute after:w-full after:h-[2px] after:border-t-primary-600 after:border-t-[2px] after:bottom-0 after:left-0'
              : ''
          "
          class="relative flex items-center justify-center h-full hover:text-primary-600 hover:after:absolute hover:after:w-full hover:after:h-[2px] hover:after:border-t-primary-600 after:transition-all after:duration-100 hover:after:border-t-[2px] hover:after:bottom-0 after:left-0"
          href="#services"
          >Services</nuxt-link
        >
        <nuxt-link
          :class="
            hashedRoute === '#request-quote'
              ? 'relative text-primary-600 after:absolute after:w-full after:h-[2px] after:border-t-primary-600 after:border-t-[2px] after:bottom-0 after:left-0'
              : ''
          "
          class="relative flex items-center justify-center h-full hover:text-primary-600 hover:after:absolute hover:after:w-full hover:after:h-[2px] hover:after:border-t-primary-600 after:transition-all after:duration-100 hover:after:border-t-[2px] hover:after:bottom-0 after:left-0"
          href="#request-quote"
          >Contact</nuxt-link
        >
      </nav>
      <div></div>
      <button
        class="flex items-center justify-center w-10 h-10 p-2 text-2xl font-semibold border rounded aspect-square md:hidden"
        @click="showDropDownNav = !showDropDownNav"
      >
        <Icon name="mingcute:menu-fill" />
      </button>

      <Common-DropDownNav v-if="showDropDownNav" />
    </div>
  </header>
</template>
