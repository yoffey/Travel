<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/201403/07/a3231208ca4095bef77068c202d95bd2.jpg_600x330_fbe0867a.jpg">
      <div class="banner-info">
        <div class="banner-title">
          香山公园(AAAA景区)
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          19
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @gallaryHidden="handleGallaryHidden"
    >
    </common-gallary>
  </div>
</template>

<script>
import CommonGallary from '@common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/201403/07/73a5487212c6f448e8a987a4a090256e.jpg_r_800x800_7dacd258.jpg', 'http://img1.qunarzz.com/wugc/p161/201208/12/846deb154eb6849093835fbb.jpg_r_800x800_691562dd.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryHidden () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    overflow: hidden
    position: relative
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .5)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
