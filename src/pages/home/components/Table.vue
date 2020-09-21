<template>
<swiper class="Table" :options="swiperOptions">
    <swiper-slide class="item-wrapper" v-for='(items,index) in pages' :key='index'>
        <div class="item" v-for="item in items" :key='item.id'>
            <span class="title">{{item.title}}</span>
            <span class="desc">{{item.desc}}</span>
        </div>
        <div v-show='index==0' class="item-bottom" >
            <img class="huiyuan" src="https://gw.alicdn.com/tfs/TB1M_pXdhv1gK0jSZFFXXb0sXXa-246-63.png_110x10000.jpg" alt="">
            <img class="qiandao" src="https://gw.alicdn.com/tfs/TB1u.ladeL2gK0jSZFmXXc7iXXa-162-63.png_110x10000.jpg" alt="">
        </div>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>

export default {
  name: 'HomeTable',
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
        if (pages[pages.length - 1].length === 9) {
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
.Table
  width 7rem
  height 4.5rem
  border-radius .2rem
  .item-wrapper
    background white
    display grid
    grid-template-rows: 1.2rem 1.2rem 1.2rem
    grid-template-columns: 1.8rem 1.8rem 1.8rem
    .item
      box-sizing border-box
      display flex
      flex-direction column
      align-items center
      border-right .005rem solid #f2f3f4
      border-bottom .005rem solid #f2f3f4
      .title
        padding .2rem 0
        color #333
        font-size .35rem
      .desc
        font-weight 200
    .item-bottom
      height .7rem
      position relative
      .huiyuan
        position absolute
        left .2rem
        bottom .05rem
      .qiandao
        position absolute
        left 3.6rem
        bottom .05rem
        height: 90%

</style>
