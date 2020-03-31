<template>
    <div class="wrapper">
        <swiper :options="swiperOptions">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" />
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: '//img1.qunarzz.com/sight/p0/1412/85/fc4b88c4d559fd35dfc0f66e0f0e2ee5.water.jpg_600x330_534f2597.jpg'
      }, {
        id: '0002',
        imgUrl: '//img1.qunarzz.com/sight/p0/1412/ad/32a5e0cd8baa07f908eab28e03d5a89f.water.jpg_600x330_353965dc.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 55.0%
    background-color: #eee
    .swiper-img
      width: 100%
</style>
