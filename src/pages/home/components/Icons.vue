<template>
<swiper class="Icons" :options="swiperOptions">
    <swiper-slide class="img-wrapper" v-for='(items,index) in pages' :key='index'>
        <div class="item" v-for="item in items" :key='item.id'>
            <img class="img" :src="item.imgUrl" alt="">
            <span class="desc">{{item.desc}}</span>
        </div>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>

export default {
  name: 'HomeIcons',
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
  },
  computed: {
    pages () {
      const pages = [[]]
      this.list.forEach((item) => {
        if (pages[pages.length - 1].length === 5) {
          pages.push([])
        }
        pages[pages.length - 1].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  .Icons
    height: 1.56rem
    .img-wrapper
      display flex
      align-items center
      justify-content flex-start
      .item
        height: 1.2rem
        width:  1.4rem
        display flex
        flex-direction column
        align-items center
        padding 0rem .05rem
        .img
          width 1.4rem
        .desc
          margin-top: .05rem

</style>
