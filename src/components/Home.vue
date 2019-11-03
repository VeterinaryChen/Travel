<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
    <home-weekend></home-weekend>
  </div>
</template>

<script>
import HomeHeader from "./child/Header";
import HomeSwiper from "./child/Swiper";
import HomeIcons from "./child/Icons";
import HomeRecommend from "./child/Recommend";
import HomeWeekend from './child/Weekend';
export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  }
};
</script>

<style>
</style>
