<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
  </div>
</template>

<script>
import HomeHeader from "./child/Header";
import HomeSwiper from "./child/Swiper";
import HomeIcons from "./child/Icons";
export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons
  }
};
</script>

<style>
</style>
