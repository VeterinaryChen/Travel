<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="(item,index) of list" :key="index">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeWeekend",
  props:{
    list: Array
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.title {
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2rem;
}

.item-img-wrapper {
  height: 0;
  overflow: hidden;
  padding-bottom: 33.9%;

  .item-img {
    width: 100%;
  }

  .item-info {
    padding: .1rem
    .item-title {
      line-height: 0.54rem;
      font-size: 0.3rem;
      ellipsis();
    }

    .item-desc {
      line-height: 0.4rem;
      color: #ccc;
      ellipsis();
    }
  }
}
</style>