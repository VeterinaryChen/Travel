<template>
  <div>
    <router-link class="header-abs" tag="div" to="/" v-show="showAbs">
      <div class="iconfont header-abs-back">&#xe6ed;</div>
    </router-link>
    <div class="header-fixed" v-show="!showAbs" :style="opacityStyle">
      <router-link to="/">
        <div class="iconfont header-fixed-back">&#xe6ed;</div>
      </router-link>
        景点详情
    </div>
  </div>
</template>

<script>
export default {
  name:'DetailHeader',
  data(){
    return {
      showAbs:true,
      opacityStyle:{
        opacity:0
      }
    }
  },
  methods:{
    handleScroll(){
      const top = document.documentElement.scrollTop;
      if(top > 60){
        let opacity = top / 140;
        opacity = opacity > 1 ? 1 : opacity;
        this.opacityStyle = {
          opacity : opacity
        }
        this.showAbs = false;
      }else{
        this.showAbs = true;
      }
    }
  }, 
  activated(){
    window.addEventListener('scroll',this.handleScroll);
  },
  deactivated(){
    window.removeEventListener('scroll',this.handleScroll);
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
  .header-abs{
    position: absolute;
    left :.2rem;
    top :.2rem;
    width: .8rem;
    height: .8rem;
    border-radius: .4rem;
    background:rgba(0,0,0,.8);
    .header-abs-back{
      color :#fff;
      font-size :.6rem;
      text-align:center;
      line-height :.8rem;
    }
  }
  .header-fixed {
  position :fixed
  top:0;
  left :0;
  right:0;
  height: $headerHeight;
  line-height: $headerHeight;
  text-align: center;
  color: #fff;
  background: $bgColor;
  font-size: 0.32rem;

  .header-fixed-back {
    position :absolute;
    width: 0.64rem;
    text-align: center;
    font-size: 0.5rem;
    top :0;
    left :0;
    color: #fff;
  }
}
</style>