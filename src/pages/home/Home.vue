<template>
<div class="home">
    <div class="top-view">
        <home-header/>
        <home-swiper :list='swiperImgs'/>
    </div>
    <home-icons :list='iconImgs'/>
    <home-table :list='tableItems'/>
    <home-recommend :list='recommendList' />
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeTable from './components/Table'
import HomeRecommend from './components/Recommend'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeTable,
    HomeRecommend
  },
  data () {
    return {
      swiperImgs: [],
      iconImgs: [],
      tableItems: [],
      recommendList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json?city=' + this.city)
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.swiperImgs = data.swiperImgs
        this.iconImgs = data.iconImgs
        this.tableItems = data.tableItems
        this.recommendList = data.recommendList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  },
  activated () {
    if (this.lastCity !== this.city) {
      this.lastCity = this.city
      this.getHomeInfo()
    }
  }
}
</script>

<style lang="stylus" scoped>
.home
  background #f2f3f4
  .top-view
    position relative
    height 3.45rem
    top 0
    background url("https://gw.alicdn.com/tfs/TB1ZPa0EzTpK1RjSZKPXXa3UpXa-750-420.png_790x10000.jpg")
</style>
