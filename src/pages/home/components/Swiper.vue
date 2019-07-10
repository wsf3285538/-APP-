<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for='item of swiperList' :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"
        />
      </swiper-slide>
      <div class="swiper-pagination swiperback"  slot="pagination"></div>
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
        setWrapperSize: true,
        paginationClickable: true,
        mousewheelControl: true,
        observeParents: true,
        autoplay: 3000,
        speed: 900,
        clickable: true,
        paginationType: 'bullets',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/4e474ded659cd8e791404278930f48d0.jpg_890x330_54c60781.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/ca4749bb92e93e2e5bf960c704b095d1.jpg_890x330_d9b4e8f3.jpg'
      }, {
        id: '0003',
        imgUrl: 'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/1a77cfc99bdf951b099c2c963729546b.jpg_890x330_3b8b02bb.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background :#fff !important
  .wrapper
    overflow :hidden
    width :100%
    height :0
    padding-bottom :31.25%
    background :#eee
    .swiper-img
      width :100%
    .swiperback
      margin-bottom :.2rem
</style>
