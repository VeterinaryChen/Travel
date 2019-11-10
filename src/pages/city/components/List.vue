<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">{{this.$store.state.city}}</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">热门城市</div>
          <div class="button-list">
            <div class="button-wrapper" v-for="item of hotCities" :key="item.id" @click="handleCityClick(item.name)">
              <div class="button">{{item.name}}</div>
            </div>
          </div>
      </div>
      <div class="area" v-for="(item,key) of cities" :key="key" :ref="key">
        <div class="title border-topbottom">{{key}}</div> 
          <div class="item-list">
            <div class="item border-topbottom" v-for="innerItem of item" :key="innerItem.id" @click="handleCityClick(innerItem.name)">
              {{innerItem.name}}
            </div>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: "CityList",
  props:{
    hotCities:Array,
    cities:Object,
    letter:String
  },
  methods:{
    handleCityClick(name){
      this.$store.dispatch('changeCity',name);
      this.$router.push('/');
    }
  },
  mounted(){
    this.scroll = new Bscroll(this.$refs.wrapper);
  },
  watch:{
    letter(){
      if(this.letter){
        const element = this.$refs[this.letter][0];
        this.scroll.scrollToElement(element);
      }
    }
  }
};
</script>

<style lang="stylus" scoped>
.border-topbottom {
  &:before {
    border-color: #ccc;
  }

  &:after {
    border-color: #ccc;
  }
}
.list{
  position :absolute;
  top: 1.58rem;
  left: 0;
  right: 0;
  bottom: 0;
  overflow: hidden;
  .title {
    line-height: 0.54rem;
    background: #eee;
    padding-left: 0.2rem;
    color: #666;
    font-size: 0.26rem;
  }
  .button-list {
    padding: 0.1rem .6rem .1rem .1rem;
    overflow: hidden;
    .button-wrapper {
      float: left;
      width: 33.33%;
      .button {
        text-align: center;
        margin: 0.1rem;
        padding: .1rem;
        border: 0.02rem solid #ccc;
      }
    }
  }
  .item-list{
    .item{
      line-height: .76rem;
      padding-left: .2rem;
    }
  }

}


</style>

 