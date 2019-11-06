<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">热门城市</div>
          <div class="button-list">
            <div class="button-wrapper">
              <div class="button">北京</div>
            </div>
            <div class="button-wrapper">
              <div class="button">北京</div>
            </div>
            <div class="button-wrapper">
              <div class="button">北京</div>
            </div>
            <div class="button-wrapper">
              <div class="button">北京</div>
            </div>
            <div class="button-wrapper">
              <div class="button">北京</div>
            </div>
          </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
          <div class="item-list">
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
          </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
          <div class="item-list">
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
          </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
          <div class="item-list">
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
          </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
          <div class="item-list">
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
          </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
          <div class="item-list">
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
            <div class="item border-topbottom">阿拉尔</div>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: "CityList",
  mounted(){
    this.scroll = new Bscroll(this.$refs.wrapper);
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

 