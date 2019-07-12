<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="(item, index) of recommendList" :key="index">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_200x200_4ab5da75.jpg',
        title: '大连圣亚海洋世界(4A)',
        desc: '浪漫大连首站，浪漫的海洋主题公园'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1808/d8/d89ec1b26e92573ea3.water.jpg_200x200_8606cb4d.jpg',
        title: '海昌发现王国',
        desc: '浪漫大连首站，奇妙的王国'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1903/89/8965f21723d9da86a3.water.jpg_200x200_90a1a827.jpg',
        title: '大连森林动物园',
        desc: '浪漫大连首站，可爱的动物主题公园'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top :.2rem
    line-height :.8rem
    background :#eee
    text-indent :.2rem
  .item
    overflow :hidden
    display :flex
    height :1.9rem
    .item-img
      width :1.7rem
      height :1.7rem
      padding :.1rem
    .item-info
      flex :1
      padding :.1rem
      min-width :0
      .item-title
        line-height :.54rem
        font-size :.32rem
        ellipsis()
      .item-desc
        line-height :.4rem
        color :#ccc
        ellipsis()
      .item-button
        line-height :.44rem
        margin-top :.16rem
        background :#ff9300
        padding :0 .2rem
        border-radius :.6rem
        color :#fff
</style>
