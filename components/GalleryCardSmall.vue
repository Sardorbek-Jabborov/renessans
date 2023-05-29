<template>
  <div class="w-[380px]">
    <img :src="img" alt="" />
    <p class="font-bold text-xl leading-130 text-white pt-4 pb-7">
      {{ title }}
    </p>
  </div>
</template>

<script setup lang="ts">
interface Props {
  img?: String
  title?: String
}
defineProps<Props>()
</script>
