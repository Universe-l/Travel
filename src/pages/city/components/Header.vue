<template>
    <div>
        <div class="header">
            <div class="header-title">
                <div class="title-left">
                    <router-link to="/">
                        <div class="iconfont back-icon">&#xe624;</div>
                    </router-link>
                </div>
                城市选择
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
  .header
    background $bgColor
    overflow hidden
  .header-title
    height .68rem
    line-height .68rem
    color white
    text-align center
    border 0
    padding-top .2rem
    font-size .3rem
    .title-left
      float left
      padding-left .2rem
      font-size .3rem
      .back-icon
        color white
</style>
