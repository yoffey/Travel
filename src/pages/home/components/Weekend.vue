<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="(item, index) of itemList" :key="'item' + index">
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
      itemList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1711/15/1cdd5ee885686b.jpg_r_640x214_46768064.jpg',
        title: '世茂云上厦门观光厅',
        desc: '厦门市思明区大学路世茂海峡大厦B塔'
      }, {
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1711/15/1cdd5ee885686b.jpg_r_640x214_46768064.jpg',
        title: '世茂云上厦门观光厅',
        desc: '厦门市思明区大学路世茂海峡大厦B塔'
      }, {
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1711/15/1cdd5ee885686b.jpg_r_640x214_46768064.jpg',
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
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.4%
  .item-img
    width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .36rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
