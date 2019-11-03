<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="(item,index) of recommendList" :key="index">
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
  data: function() {
    return {
      recommendList: [
        {
          id: "0001",
          imgUrl:
            "https://imgs.qunarzz.com/sight/p0/1910/6f/6f3fa8d8f8e14b66a3.water.jpg_200x200_4f294e8c.jpg",
          title: "观澜山水田园旅游文化园",
          desc: "观澜山水田园旅游文化园desc"
        },
        {
          id: "0002",
          imgUrl:
            "https://imgs.qunarzz.com/sight/p0/1910/6f/6f3fa8d8f8e14b66a3.water.jpg_200x200_4f294e8c.jpg",
          title: "观澜山水田园旅游文化园",
          desc: "观澜山水田园旅游文化园desc"
        },
        {
          id: "0003",
          imgUrl:
            "https://imgs.qunarzz.com/sight/p0/1910/6f/6f3fa8d8f8e14b66a3.water.jpg_200x200_4f294e8c.jpg",
          title: "观澜山水田园旅游文化园",
          desc: "观澜山水田园旅游文化园desc"
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.title {
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2rem;
  margin-top: 0.2rem;
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
</style>ß