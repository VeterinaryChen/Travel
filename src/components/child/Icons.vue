<template>
    <div class="icons">
        <swiper>
            <swiper-slide v-for="(page,index) of pages" :key="index">
                <div class="icon" v-for="item of page" :key="item.id">
                    <div class="icon-img">
                        <img class="icon-img-content" :src="item.img">
                    </div>
                    <p class="icon-desc">{{item.desc}}</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>
<script>
export default {
    name: 'HomeIcons',
    data: function(){
        return {
            iconList: [
            {
                id: '0001',
                img: 'https://imgs.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                desc: '景点门票'
            },
            {
                id: '0002',
                img: 'https://imgs.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
                desc: '深圳必游'
            },
            {
                id: '0003',
                img: 'https://imgs.qunarzz.com/piao/fusion/1803/12/216ce2e78b5f5f02.png',
                desc: '万圣狂欢'
            },
            {
                id: '0004',
                img: 'https://imgs.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
                desc: '海洋馆'
            },
            {
                id: '0005',
                img: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/b0026eb6f96fd2daecba0d7982c7e4c8.png',
                desc: '约惠深圳'
            },
            {
                id: '0006',
                img: 'https://imgs.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
                desc: '深圳欢乐谷'
            },
            {
                id: '0007',
                img: 'https://imgs.qunarzz.com/piao/fusion/1803/a6/6d97515091789602.png',
                desc: '世界之窗'
            },
            {
                id: '0008',
                img: 'https://imgs.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
                desc: '东部华侨城'
            },
            {
                id: '0009',
                img: 'https://imgs.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                desc: '一日游'
            },
            ]
        }
    },
    computed:{
        pages (){
            const pages = []
            this.iconList.forEach((item,index) => {
                const page = Math.floor(index/8);
                if(!pages[page]){
                    pages[page] = []
                }
                pages[page].push(item)
            })
            return pages
        }
    }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
.icons >>> .swiper-container
    height:0
    padding-bottom :50%
.icon
    position: relative
    overflow hidden
    width: 25%
    float: left
    padding-bottom :25%
    height: 0
    .icon-img
        position: absolute
        top: 0
        left: 0 
        right: 0
        bottom: 0.44rem
        box-sizing: border-box
        padding: 0.1rem
        .icon-img-content
            height: 100%
            display :block
            margin: 0 auto 
    .icon-desc
        position: absolute
        left: 0 
        right: 0
        bottom: 0
        height: 0.44rem
        line-height: 0.44rem
        color: $darkTextColor
        text-align: center
        ellipsis()
</style>