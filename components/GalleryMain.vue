<template>
  <swiper
    :modules="modules"
    :slides-per-view="1"
    :space-between="0"
    :controller="isLeftHandSideExpression"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide v-for="obj in GalleryCardMain" :key="obj.title">
      <GalleryCardMain :img="obj.img" :title="obj.title" />
    </swiper-slide>
  </swiper>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue'
import GalleryCardMain from './GalleryCardMain.vue'
import { A11y } from 'swiper'
// Import Swiper styles
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
import 'swiper/css/scrollbar'

export default {
  components: {
    Swiper,
    SwiperSlide,
    GalleryCardMain,
  },
  modules: [A11y],

  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper)
    }
    const onSlideChange = () => {
      console.log('slide change')
    }

    const GalleryCardMain = [
      {
        title: 'Kansert Hall',
        img: '/png/gallery-1.png',
      },
      {
        title: 'banket Hall',
        img: '/png/gallery-2.png',
      },
      {
        title: 'present Hall',
        img: '/png/gallery-3.png',
      },
    ]
    return {
      onSwiper,
      onSlideChange,
      GalleryCardMain,
    }
  },
}
</script>
