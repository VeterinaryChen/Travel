<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe6ed;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe70a;</span>
      输入城市/经典/游玩</div>
    <router-link to="/city">
      <div class="header-right">
        {{this.$store.state.city}}
        <span class="iconfont down-icon">&#xe6f8;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import {mapState} from 'vuex';
export default {
  name: 'HomeHeader',
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header 
    display: flex;
    line-height: $headerHeight;
    background:$bgColor;
    color:#fff;
    .header-left 
      width: .64rem;
      float :left;
      .back-icon
        text-align: center;
        font-size: 0.5rem;
    .header-input 
      flex: 1;
      height: .64rem ;
      line-height:  .64rem;
      background:#fff ;
      margin-top:.12rem; 
      margin-left:.2rem ;
      background:#fff ;
      border-radius:.1rem;
      color: #ccc;
    .header-right 
      min-width :1.04rem;
      padding: 0.1rem
      float: right ;
      text-align:center;
      color: #fff
      .down-icon
        text-align: center;
        font-size: 0.5rem;
      
</style>
