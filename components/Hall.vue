<template>
  <div
    class="h-[500px] relative flex flex-col w-[50vw] style-linear"
    :image="image"
  >
    <div class="absolute top-0 left-0 z-[-1] h-full w-full">
      <img :src="image" alt="" class="w-full h-full" />
    </div>

    <div class="!mt-auto !mb-[50px] !pl-[120px] maw-w-[470px]">
      <h1 class="font-normal text-[32px] leading-130 text-white uppercase pb-1">
        hi
      </h1>
      <p class="font-light text-xs leading-140 text-white w-[460px] pb-[40px]">
        Hashamatli Renesans Hall saroyi 2500 kvadrat metrli monitorlar, 1500 dan
        ortiq professional yoritish uskunalari, lazer shoulari, o‘ta zamonaviy
        ovoz uskunalari
      </p>

      <MButton title="Batafsil ko‘rish" icon=" /svg/arrow-right.svg" />
    </div>
  </div>
</template>
<style scoped>
.style-linear {
  background: linear-gradient(
    180deg,
    rgba(2, 17, 23, 0) 0%,
    rgba(2, 17, 23, 0.8) 100%
  );
  mix-blend-mode: normal;
}
</style>

<script lang="ts">
import MButton from './Button/MButton.vue'
export default {
  props: {
    image: {
      type: String,
      requried: true,
    },
  },
  components: {
    MButton,
  },
}
</script>
