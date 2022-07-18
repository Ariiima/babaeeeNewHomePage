<template>
  <swiper
    :slides-per-view="1"
    :space-between="80"
    :navigation="true"
    :loop="true"
    :pagination="{
      clickable: true,
    }"
    :modules="modules"
  >
    <swiper-slide>
        <img src="../assets/photo.png" class="w-[70rem] mx-auto pb-[3rem]" />
    </swiper-slide>
    <swiper-slide>
        <img src="../assets/photo.png" class="w-[70rem] mx-auto pb-[3rem]" />
    </swiper-slide>
    <swiper-slide>
        <img src="../assets/photo.png" class="w-[70rem] mx-auto pb-[3rem]" />
    </swiper-slide>
  </swiper>
</template>
<script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';
  import "swiper/css/navigation"; 
  import "swiper/css/pagination";
  import { Pagination,Navigation } from "swiper";
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Pagination,Navigation],
      };
    },
  };
</script>

