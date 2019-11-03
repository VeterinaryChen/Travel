<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="(item,index) of recommendList" :key="index">
        <img
          class="item-img"
          :src="item.imgUrl"
        />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  data:function(){
    return {
      recommendList : [
      {
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1910/6f/6f3fa8d8f8e14b66a3.water.jpg_200x200_4f294e8c.jpg',
        title: '观澜山水田园旅游文化园',
        desc: '观澜山水田园旅游文化园desc'
      },
      {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1910/6f/6f3fa8d8f8e14b66a3.water.jpg_200x200_4f294e8c.jpg',
        title: '观澜山水田园旅游文化园',
        desc: '观澜山水田园旅游文化园desc'
      },
      {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1910/6f/6f3fa8d8f8e14b66a3.water.jpg_200x200_4f294e8c.jpg',
        title: '观澜山水田园旅游文化园',
        desc: '观澜山水田园旅游文化园desc'
      },
      ]
    }
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title {
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2rem;
  margin-top: 0.2rem;
}

.item {
  display: flex;
  height: 1.9rem;
  overflow: hidden;

  .item-img {
    width: 1.7rem;
    height: 1.7rem;
    padding: 0.1rem;
  }

  .item-info {
    flex: 1;
    padding: 0.1rem;
    min-width :0

    .item-title {
      line-height: 0.54rem;
      font-size: 0.3rem;
      ellipsis()
    }

    .item-desc {
      line-height: 0.4rem
      color: #ccc
      ellipsis()
    }

    .item-button {
      margin-top: 0.16rem
      background: #ff9300
      padding: 0.2rem
      border-radius: .26rem
      line-height :.44rem
    }
  }
}
</style>