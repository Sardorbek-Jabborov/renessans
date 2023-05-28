<template>
  <!-- <NuxtLayout>
    <div>
      <NuxtPage />
    </div>
  </NuxtLayout> -->
  <!-- <About />
  <Gallery /> -->
  <GalleryMain />
</template>

<script setup>
import About from './components/About.vue'
import Gallery from './components/Gallery.vue'
import GalleryMain from './components/GalleryMain.vue'
import { onMounted } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()

if ('setup' in route.query) {
  throw new Error('error in setup')
}
if ('mounted' in route.query) {
  onMounted(() => {
    throw new Error('error in mounted')
  })
}
</script>
