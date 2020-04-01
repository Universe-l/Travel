<template>
    <div>
       <div class="tittle">热销推荐</div>
       <ul>
           <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
               <img class="item-img" :src="item.imgUrl" />
               <div class="item-info">
                   <p class="item-tittle">{{item.tittle}}</p>
                   <p class="item-desc">{{item.desc}}</p>
                   <button class="item-btn">查看详情</button>
               </div>
           </li>
       </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1507/cc/19733fc0135062788140cbb48ae606a7.water.jpg_200x200_d9ebe2fd.jpg',
        tittle: '北京野生动物园',
        desc: '敢与森林之王近距离接触吗？'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_200x200_2458ffb2.jpg',
        tittle: '八达岭长城',
        desc: '不到长城非好汉'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1505/d2/d274c92de14c93da.water.jpg_200x200_2cce447f.jpg',
        tittle: '颐和园',
        desc: '中国现存最大的皇家园林'
      }, {
        id: '0004',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1505/f5/f5f45e1a83537bcb.water.jpg_200x200_444cc7e8.jpg',
        tittle: '圆明园',
        desc: '百年皇家的珍宝,民族耻辱的见证'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';
  .tittle
    line-height: .8rem
    background-color: #eeeeee
    text-indent: .2rem
    margin-top: .2rem
  .item
    display: flex
    height: 1.9rem
    overflow: hidden
    padding-bottom .2rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding .1rem
    .item-info
      padding 0 .1rem
      min-width 0
      .item-tittle
        height .44rem
        line-height .44rem
        font-size .32rem
        color $darkTextColor
        margin-top .26rem
        ellipsis()
      .item-desc
        font-size .24rem
        line-height .34rem
        margin-top .26rem
        color #cccccc
        ellipsis()
      .item-btn
        font-size .24rem
        padding 0 .2rem
        border-radius .1rem
        color white
        margin-top 0.15rem
        background #ff9300
</style>
