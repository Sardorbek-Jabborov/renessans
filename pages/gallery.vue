<template>
  <div class="container !mt-10">
    <h1
      class="font-normal text-[32px] leading-[29px] text-white pb-6 uppercase"
    >
      galereya
    </h1>
    <div class="flex justify-between flex-wrap">
      <div v-for="obj in GalleryCard" :key="obj.title">
        <GalleryCardSmall :img="obj.img" :title="obj.title" />
      </div>
    </div>
  </div>
</template>

<script setup>
import GalleryCardSmall from '../components/GalleryCardSmall.vue'

const GalleryCard = [
  {
    img: '/png/gallery-1.png',
    title: 'Konsert Hall',
  },
  {
    img: '/png/gallery-2.png',
    title: 'Banket Hall',
  },

  {
    img: '/png/gallery-3.png',
    title: 'Taqdimotlar zali',
  },

  {
    img: '/png/gallery-4.png',
    title: 'Konsert Hall',
  },
  {
    img: '/png/gallery-5.png',
    title: 'Banket Hall',
  },

  {
    img: '/png/gallery-6.png',
    title: 'Taqdimotlar zali',
  },
]
</script>
