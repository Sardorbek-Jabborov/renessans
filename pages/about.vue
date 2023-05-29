<template>
  <div>
    <AboutUs />
    <AboutInfo />
    <div class="flex">
      <Hall class="" image="/png/gallery-2.png" />
      <Hall class="" image="/png/gallery-1.png" />
    </div>
  </div>
</template>

<script setup lang="ts">
import { definePageMeta } from '#imports'
import AboutUs from '../components/AboutUs.vue'
import AboutInfo from '../components/AboutInfo.vue'
import Hall from '../components/Hall.vue'
definePageMeta({
  layout: 'custom',
})
</script>
