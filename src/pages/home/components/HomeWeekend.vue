<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="(item, index) of weekendList" :key="index">
        <div class="item-img-wrapper">
           <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
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
      weekendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1812/b4/e9d7f043c4fadf.jpg_r_640x214_713df0cf.jpg',
        title: '大连泡汤圣地',
        desc: '享受生活，放松自己，来一段轻松的旅程。'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7f/fa4eb0ca72409d.jpg_r_640x214_2f2a860e.jpg',
        title: '大连必打卡',
        desc: '爱上北方的碧海蓝天'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/b7/8a08a1023062b3.jpg_r_640x214_d7cb475c.jpg',
        title: '最赞的海滨浴场',
        desc: '跳进海里，享受铺天盖地的清凉吧'
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
  .item-img-wrapper
    overflow :hidden
    height :0
    padding-bottom :33.9%
  .item-img
    width :100%
  .item-info
    padding :.1rem
    .item-title
      line-height :.54rem
      font-size :.32rem
      ellipsis()
    .item-desc
      line-height :.4rem
      color :#ccc
      ellipsis()
</style>
