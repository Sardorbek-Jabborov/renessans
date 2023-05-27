<template>
  <div class="w-[380px]">
    <img :src="img" alt="" />
    <p class="font-bold text-xl leading-130 text-white pt-4 pb-7">
      {{ title }}
    </p>
  </div>
</template>

<script lang="ts">
export default {
  props: {
    img: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
  },
}
</script>
