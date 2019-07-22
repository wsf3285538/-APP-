<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="https://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_600x330_93d96bdf.jpg"/>
      <div class="banner-info">
        <div class="banner-title">北京欢乐谷(AAAA景区)</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          27
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1906/e7/e7276de002459b50a3.img.jpg_350x240_dd696261.jpg', 'http://img1.qunarzz.com/sight/p0/1906/cd/cdc0a756c33a26cfa3.img.jpg_350x240_5de2d8cd.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position :relative
    overflow :hidden
    height :0
    padding-bottom :55%
    .banner-img
      width :100%
    .banner-info
      display :flex
      position :absolute
      left :0
      right :0
      bottom :0
      line-height :.6rem
      color :#fff
      background-image :linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex :1
        font-size :.32rem
        padding :0 .2rem
      .banner-number
        height :.32rem
        line-height :.4rem
        margin-top :.14rem
        padding :0 .4rem
        border-raduis :.2rem
        background :rgba(0, 0, 0, .8)
        font-size :.24rem
        .banner-icon
          font-size :.24rem
</style>
