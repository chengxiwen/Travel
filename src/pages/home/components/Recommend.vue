<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" src='item.imgUrl' />
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
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1410/09/15eb4e4c3f0d581283fffcfff300e2af.jpg_200x200_62c5db37.jpg',
        title: '子胥湖欢乐嘉年华',
        desc: '景色优美，旅游胜地'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/6b/6b37d02f8028b093a3.img.jpg_200x200_a131d7fc.jpg',
        title: '子胥湖欢乐嘉年华',
        desc: '景色优美，旅游胜地'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/6b/6b37d02f8028b093a3.img.jpg_200x200_a131d7fc.jpg',
        title: '子胥湖欢乐嘉年华',
        desc: '景色优美，旅游胜地'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
