<template>
    <div>
       <div class="tittle">周末去哪儿</div>
       <ul>
           <li class="item border-bottom" v-for="item of weekendList" :key="item.id">
               <div class="item-img-wraper">
                   <img class="item-img" :src="item.imgUrl" />
               </div>
               <div class="item-info">
                   <p class="item-tittle">{{item.title}}</p>
                   <p class="item-desc">{{item.desc}}</p>
               </div>
           </li>
       </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
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
  .item-img-wraper
    height 0
    padding-bottom 33.4%
    overflow hidden
    .item-img
      width 100%
  .item-info
    flex 1
    padding 0 .1rem
    min-width 0
    .item-tittle
      height .44rem
      line-height .44rem
      font-size .32rem
      color $darkTextColor
      padding-top .3rem
      ellipsis()
    .item-desc
      font-size .24rem
      line-height .34rem
      margin-top .1rem
      color #cccccc
      ellipsis()
      padding-bottom .3rem
</style>
