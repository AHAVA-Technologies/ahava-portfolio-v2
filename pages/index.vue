<template>
  <div>
    <div
      class="px-5 w-full !overflow-x-hidden xl:px-36 lg:px-20 md:px-10 space-y-10"
    >
      <Landing-Hero />
      <Landing-About />
      <Landing-WhyChooseUs />
      <Landing-Services />
      <Landing-RequestQuote />
      <Landing-Teams :members="members" />
    </div>
  </div>
</template>

<script lang="ts" setup>
const members = ref([
  {
    image: "/img/zerubabel.jpg",
    name: "Zerubabel Kassahun",
    role: "Systems Engineer",
  },
  {
    image: "/img/samuel.jpg",
    name: "Samuel Noah",
    role: "Graphics Designer",
  },
  {
    image: "/img/yonatan.jpg",
    name: "Yonatan Tesfaye",
    role: "Web Developer",
  },
  {
    image: "/img/sami.bmp",
    name: "Samuel Melis",
    role: "Graphics Designer",
  },
  {
    image: "/img/abel.jpg",
    name: "Abel Abebe",
    role: "Mobile Developer",
  },
  {
    image: "/img/jamie.jpg",
    name: "Mintesnot Markos",
    role: "Web Developer",
  },
  {
    image: "/img/yonas.jpg",
    name: "Yonas Sisay",
    role: "Mobile Developer",
  },
]);
</script>
