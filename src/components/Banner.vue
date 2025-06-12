<template>
  <div class="banner">
    <swiper
      :modules="modules"
      :loop="true"
      :autoplay="{ delay: 7000 }"
      :pagination="{ clickable: true }"
      class="banner-swiper"
    >
      <swiper-slide v-for="(img, index) in images" :key="index">
        <img :src="img" alt="banner" />
      </swiper-slide>
    </swiper>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination } from "swiper/modules";
import "swiper/swiper-bundle.css";

const modules = [Autoplay, Pagination];
const images = [
  new URL("@/assets/images/banner.jpg", import.meta.url).href,
  new URL("@/assets/images/banner.jpg", import.meta.url).href,
  new URL("@/assets/images/banner.jpg", import.meta.url).href,
];
</script>

<style lang="scss" scoped>
.banner {
  margin-top: -94px;
  @media (max-width: 767px) {
    margin-top: 0;
    background-color: #f64c24;
  }

  .banner-swiper {
    width: 100%;
    height: auto;

    img {
      width: 100%;
      display: block;
    }

    // 讓點點區塊有寬高
    ::v-deep(.swiper-pagination) {
      position: absolute;
      bottom: 10px;
      left: 0;
      width: 100%;
      height: 30px;
      text-align: center;
      z-index: 10;
    }

    // 點點樣式
    ::v-deep(.swiper-pagination-bullet) {
      background: rgba(255, 255, 255, 0.6);
      margin: 0 4px;
      width: 10px;
      height: 10px;
      opacity: 1;
      border-radius: 50%;
      display: inline-block;
    }

    ::v-deep(.swiper-pagination-bullet-active) {
      background: #ff714a;
    }
  }
}
</style>
