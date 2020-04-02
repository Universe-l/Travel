<template>
    <div class="header">
      <div class="header-left">
        <div class="iconfont back-icon">&#xe624;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩/主题</div>
      <div class="header-right">
        {{city}}
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl';
  .header
    display: flex
    height: .86rem
    line-height: .86rem
    background: $bgColor
    color: white
    .header-input
      flex: 1
      height: .60rem
      color: #cccccc
      line-height: .60rem
      margin-top: .12rem
      margin-left: .2rem
      margin-right: .2rem
      background: #ffffff
      border-radius: .1rem
      padding-left: .2rem
    .header-left
      height: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
    .header-right
      height: 1.44rem
      float: right
      text-align: center
      margin-right: .2rem
      .arrow-icon
        font-size: .2rem
</style>
