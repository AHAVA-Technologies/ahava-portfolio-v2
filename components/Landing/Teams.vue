<template>
  <Carousel
    :breakpoints="breakpoints"
    :wrapAround="true"
    :transition="500"
    id="teams"
  >
    <Slide
      v-for="(member, i) in members"
      :key="i"
      :class="`grid grid-cols-${members.length}`"
    >
      <div class="carousel__item draggable">
        <Landing-TeamMember :member="member" />
      </div>
    </Slide>
    <template #addons>
      <Pagination />
    </template>
  </Carousel>
</template>

<script lang="ts" setup>
import { Carousel, Pagination, Slide } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

defineProps({
  members: {
    type: Array as PropType<any>,
    required: true,
  },
});

const breakpoints = ref({
  320: {
    itemsToShow: 1.3,
    snapAlign: "center",
  },
  768: {
    itemsToShow: 2,
    snapAlign: "center",
  },
  1024: {
    itemsToShow: 3,
    snapAlign: "center",
  },
});
</script>

<style>
.carousel__slide {
  padding: 5px;
}

.carousel__viewport {
  perspective: 2000px;
}

.carousel__track {
  transform-style: preserve-3d;
}

.carousel__slide--sliding {
  transition: 0.5s;
}

.carousel__slide {
  opacity: 0.9;
  transform: rotateY(-20deg) scale(0.9);
}

.carousel__slide--active ~ .carousel__slide {
  transform: rotateY(20deg) scale(0.9);
}

.carousel__slide--prev {
  opacity: 1;
  transform: rotateY(-10deg) scale(0.95);
}

.carousel__slide--next {
  opacity: 1;
  transform: rotateY(10deg) scale(0.95);
}

.carousel__slide--active {
  opacity: 1;
  transform: rotateY(0) scale(1.03);
}

.carousel__pagination-button::after {
  @apply !w-2 !bg-primary-300 rounded-md;
}
.carousel__pagination-button--active::after {
  @apply !w-4 !bg-primary-600 rounded-md;
}
</style>
