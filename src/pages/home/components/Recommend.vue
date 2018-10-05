<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="(item, index) of itemList" :key="'item' + index">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-detail-btn">查看详情</button>
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
      itemList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/7d/7dca9c37a87479eba3.img.jpg_200x200_f62f78bd.jpg',
        title: '世茂云上厦门观光厅',
        desc: '厦门市思明区大学路世茂海峡大厦B塔'
      }, {
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/7d/7dca9c37a87479eba3.img.jpg_200x200_f62f78bd.jpg',
        title: '世茂云上厦门观光厅',
        desc: '厦门市思明区大学路世茂海峡大厦B塔'
      }, {
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/7d/7dca9c37a87479eba3.img.jpg_200x200_f62f78bd.jpg',
        title: '世茂云上厦门观光厅',
        desc: '厦门市思明区大学路世茂海峡大厦B塔'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@styles/mixins.styl'
  .title
    margin-top: .2rem
    height: .8rem
    line-height: .8rem
    padding-left: .26rem
    background: #F5F5F5
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
        font-size: .36rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-detail-btn
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
