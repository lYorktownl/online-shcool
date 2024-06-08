<template>
  <swiper :slides-per-view="1" navigation pagination>
    <swiper-slide>
      <div>Слайд 1</div>
    </swiper-slide>
    <swiper-slide>
      <div>Слайд 2</div>
    </swiper-slide>
    <swiper-slide>
      <div>Слайд 3</div>
    </swiper-slide>
  </swiper>
</template>

<script>

import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/swiper-bundle.css";
export default {
  components: {
    Swiper,
    SwiperSlide,
  }
};
</script>

<style scoped>

</style>