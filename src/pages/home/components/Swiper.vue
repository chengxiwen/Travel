<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" />
            </swiper-slide>
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/9f49524e-c25d-460f-b578-1349af3f9115.jpg_r_480x320x90_a9ba090a.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/p/tts0/1810/26/3c6d0e9342a45202.jpg_r_480x320x90_6b7e0634.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
        background: #fff
    .wrapper
        overflow: hidden
        width: 100%
        height: 0
        padding-bottom: 31.25%
        .swiper-img
            width: 100%
            height: 2.0rem
</style>
