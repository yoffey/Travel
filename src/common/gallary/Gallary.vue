<template>
  <div class="container" @click='handleContainerClick'>
    <div class="wrapper">
      <swiper :options="swiperOptions" v-if="this.imgs.length">
        <swiper-slide v-for="(item, index) in imgs" :key="index">
          <img class="gallary-img" :src="item">
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommonGallary',
  props: {
    imgs: {
      type: Array,
      default () {
        return []
      }
    }
  },
  data () {
    return {
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination',
          type: 'fraction'
        },
        loop: true,
        observer: true,
        observeParents: true
      }
    }
  },
  methods: {
    handleContainerClick () {
      this.$emit('gallaryHidden')
    }
  }
}
</script>

<style lang="stylus" scoped>
  .container >>> .swiper-container
    overflow: inherit
  .container
    display: flex
    flex-direction: column
    justify-content: center
    z-index: 99
    position: fixed
    top: 0
    right: 0
    bottom: 0
    left: 0
    background: #000
    .wrapper
      // overflow: hidden
      height: auto
      width: 100%
      // padding-bottom: 100%
      .gallary-img
        width: 100%
      .swiper-pagination
        color: #fff
        bottom: -1rem
</style>
