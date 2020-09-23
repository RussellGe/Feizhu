<template>
<div class="recommend">
    <div class="title">
        热销推荐
    </div>
    <div class="item" v-for='item in list' :key='item.id'>
        <img :src="item.imgUrl" class="img"/>
        <div class="content">
            <div class="content-title">{{item.title}}</div>
            <div class="content-description">{{item.desc}}</div>
            <span class="content-btn">了解详情</span>
        </div>
    </div>
</div>
</template>

<script>

export default {
  name: 'Recommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
.recommend
  padding .3rem
  .title
    font-size .45rem
    font-weight 500
  .item
    display flex
    margin .2rem 0
    border-radius .2rem
    background white
    height 2.4rem
    box-sizing border-box
    padding .1rem
    .img
      border-radius .1rem
      height 2.2rem
    .content
      box-sizing border-box
      padding .2rem
      display flex
      flex-direction column
      justify-content space-around
      .content-title
        font-size .32rem
        font-weight bold
      .content-btn
        background orange
        width 1.4rem
        display flex
        justify-content center
        align-items center
        padding .03rem .02rem
        border-radius .1rem
</style>
