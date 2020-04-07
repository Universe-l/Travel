<template>
    <div class="banner">
        <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1507/cc/19733fc0135062788140cbb48ae606a7.water.jpg_600x330_1abc2773.jpg" />
        <div class="banner-info">
            <div class="banner-title">
                北京野生动物园(AAAA景区)
            </div>
            <div class="banner-number">
                <span class="iconfont arrow-icon banner-icon">&#xe6e5;</span>
                39
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'DetailBanner'
}
</script>

<style lang="stylus" scoped>
  .banner
    overflow hidden
    height 0
    padding-bottom 55%
    position relative
    .banner-img
      width 100%
    .banner-info
      position absolute
      display flex
      left 0
      right 0
      bottom 0
      line-height .6rem
      color #ffffff
      background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.5))
      .banner-title
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-number
        padding .1rem .4rem
        line-height .32rem
        height .32rem
        font-size .24rem
        border-radius .2rem
        background rgba(0, 0, 0, .5)
        bottom 0
        margin-right .2rem
        .banner-icon
          font-size .24rem
</style>
