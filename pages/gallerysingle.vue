<template>
  <Swiper
    :modules="modules"
    :slides-per-view="1"
    :space-between="0"
    :pagination="{ clickable: true }"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide v-for="obj in GalleryCardMain" :key="obj.title">
      <GalleryCardMain :img="obj.img" :title="obj.title" />
    </swiper-slide>
  </Swiper>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue'
import GalleryCardMain from '../components/GalleryCardMain.vue'
import { A11y, Pagination } from 'swiper'
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
  modules: [Pagination, A11y],

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
