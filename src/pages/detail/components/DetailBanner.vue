<template>
  <div>
    <div class="banner" @click="handleBannerClick"> 
      <img 
      class="banner-img"
      :src="bannerImg"/>
      <div class="banner-info">
        <div class="banner-title">{{this.sightName}}</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe70a;</span>{{this.bannerImgs.length}}</div>
      </div>
    </div>
    <common-gallery :imgs="bannerImgs" v-show="showGallery" @close="handleGalleryClose"></common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  data(){
    return {
      showGallery:false
    }
  },
  props:{
    sightName:String,
    bannerImg:String,
    bannerImgs:Array
  },
  methods:{
    handleBannerClick(){
      this.showGallery = true;
    },
    handleGalleryClose(){
      this.showGallery = false;
    }
  },
  mounted(){
    console.log(this.bannerImgs);
  },
  components:{
    CommonGallery
  }
  
}
</script>

<style lang="stylus" scoped>
  .banner{
    position :relative;
    overflow: hidden;
    height:0;
    padding-bottom: 55%;
    .banner-img{
      width:100%
    }
    .banner-info{
      position :absolute;
      left :0;
      right :0;
      bottom: 0;
      line-height : .6rem;
      display :flex;
      color :#fff;
      background-image : linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
      .banner-title{
        flex :1;
        font-size :.32rem;
        padding :.2rem;
      }
      .banner-number{
        margin-top :.35rem;
        padding :0 .4rem;
        line-height : .32rem;
        height : .32rem;
        border-radius :.2rem;
        background : rgba(0,0,0,.8);
        font-size :.24rem;
        .banner-icon{
          font-size :.24rem;
        }
      }
    }
  }
</style>