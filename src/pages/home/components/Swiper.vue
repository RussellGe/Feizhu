<template>
<swiper class="mySwiper" :options="swiperOptions">
    <swiper-slide class="img-wrapper" v-for='item in list' :key='item.id'>
        <img class="swiper-img" :src="item.imgUrl" alt="">
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>

export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination'
        }
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .mySwiper
    height 2.2rem
    padding-top .1rem
    .img-wrapper
      display flex
      justify-content center
      .swiper-img
        width 7.02rem
        height 100%
        border-radius .2rem
</style>
