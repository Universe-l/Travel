<template>
    <div>
       <div class="tittle">热销推荐</div>
       <ul>
           <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
               <img class="item-img" :src="item.imgUrl" />
               <div class="item-info">
                   <p class="item-tittle">{{item.title}}</p>
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
  props: {
    recommendList: Array
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
