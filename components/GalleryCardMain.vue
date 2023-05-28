<template>
  <div class="flex flex-col container !mt-5">
    <h2
      class="font-normal text-[32px] leading-[29px] text-white pb-16 uppercase"
    >
      {{ title }}
    </h2>

    <img :src="img" alt="" class="w-[880px] h-[450px]" />
  </div>
</template>

<script lang="ts">
export default {
  props: {
    title: {
      type: String,
      required: true,
    },

    img: {
      type: String,
      required: true,
    },
  },
}
</script>
