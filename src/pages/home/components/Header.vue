<template>
    <div class="header">
      <div class="header-left">
        <div class="iconfont back-icon">&#xe624;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩/主题
      </div>
      <router-link to="/city">
        <div class="header-right">
          {{this.city}}
          <span class="iconfont arrow-icon">&#xe64a;</span>
        </div>
      </router-link>
    </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
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
      color: white
      .arrow-icon
        font-size: .2rem
</style>
