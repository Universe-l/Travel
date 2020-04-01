<template>
    <div>
       <div class="tittle">周末去哪儿</div>
       <ul>
           <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
               <div class="item-img-wraper">
                   <img class="item-img" :src="item.imgUrl" />
               </div>
               <div class="item-info">
                   <p class="item-tittle">{{item.tittle}}</p>
                   <p class="item-desc">{{item.desc}}</p>
               </div>
           </li>
       </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/86/57819390ea997c.jpg_r_640x214_00888590.jpg',
        tittle: '郑州打卡',
        desc: '日月轮回，孕育出新的美丽'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/d2/017059dd59b0ee.jpg_r_640x214_497664a4.jpg',
        tittle: '城中碧玉万仙山',
        desc: '清幽山乡，人间仙境，世外桃源，雄壮而苍茫的红崖绝壁，妙曼而秀雅的山乡风韵，太行风光的典型代表'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/2c/e5e2b086fc0c60.jpg_r_640x214_811a2da7.jpg',
        tittle: '石刻艺术宝库',
        desc: '这里是中国石刻艺术宝库，石窟的规模大、艺术精湛，石刻艺术奇葩，是石刻艺术的典范之作。'
      }, {
        id: '0004',
        imgUrl: 'https://imgs.qunarzz.com/sight/source/1603/89/a64d5966351b04.jpg_r_640x214_45776b4c.jpg',
        tittle: '焦作打卡',
        desc: '山水焦作，太极故里'
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
