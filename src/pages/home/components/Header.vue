<template>
<div class="header">
    <img class="brand" src="https://gw.alicdn.com/tfs/TB11icBexD1gK0jSZFsXXbldVXa-94-40.png" alt="飞猪">
    <div class="search">
        <img class="search-img" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB4AAAAeBAMAAADJHrORAAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAwUExURUdwTGlpaWdnZ2dnZ2ZmZmZmZmZmZnBwcGhoaGdnZ2dnZ2ZmZmxsbGdnZ2dnZ2ZmZgmtyTYAAAAPdFJOUwAiUXvR3vMGN2an6hCPubZYcwsAAAD3SURBVBjTY2BgYGDXdf3tpcMAA+yz/wPBNxsYX+T/t7W2q///boBwOfK/qAOpvv8/IXyx/wZgWu2/Alh3/CeYukQQxQyVZmDQ/wUij32Bmcv1H2Si/icYnxGscn063CH+DiDiAZxv/wFI7L8A58//CCTy0fjxCxDq/wCJ9w5w/voNIMGPcH/mg5TK/4XxOcEe4PsP9SfD6a8FYFfFQJW/h7jU/osAmD73H2IT7/+dIHVM8f99oNb+j2082Oz/Px6qkMkfFJ7/d/L+D4QoYHoG5HoWMNz/KgA1umlSDzioAhlQgP1vARQ+8/8dqArmf0Hlc2ah8hkKAIzOXNKx9n7VAAAAAElFTkSuQmCC" alt="">
        <input class="search-input" type="text"/>
    </div>
    <div class="user">
        <span class="city-name">上海</span>
        <img class="city-img" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwBAMAAAClLOS0AAAABGdBTUEAALGPC/xhBQAAAAFzUkdCAK7OHOkAAAAtUExURUdwTDQ0NDMzMzQ0NDMzMzQ0NDMzMzw8PDMzMzMzMzY2NjQ0NDMzMzMzMzMzMwhYo1AAAAAOdFJOUwDA/HXpPbALmdIhW56MA3IOiwAAAV1JREFUOMu1lL1KA1EQha8ka2JsDErEJsUSBQuHCGqhsEhExGYJGrATo02qEEHBMlVsVawlYC8Be5/BJxAcY0CF8wxu9sfdezNgo9PscL+ds3NnDqvUf8R+J+/Hs36cWYENP6Z0UEMUOkjZjN2h0IwBHPTX/WRMBxbhUkngjN6UCBy0ZeCWWiKwECkZIIVPGWRpUwbjdPUrmOAjWSrNbfnjDyjL7TqoihfMVPpKHEk2rtWH6PCOksZ+Aa4qYVH3rqEUrvYWZJdN84Rm2B5x1dA+NrZaouEaq8Kx9dipFxobRk8qt0yekqfF013t9SJHPqTXRFGuSSCUrucqYPAgrqkR908Ohtn5mkv80/KkzXG9VSS7F+Z7+EjoWneYD9MbzCY7OcVitNeBdt9MM9xuGvoKvOUE1jiEMdEU3v3nC3eNedKS/zzmvBG0EACMRACeyDznr+DidVOq0PvTP8s3+V20chwLWVgAAAAASUVORK5CYII=" alt="">
    </div>
</div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    height .88rem
    display flex
    padding .1rem
    justify-content space-around
    align-items center
    box-sizing border-box
    .brand
      height .4rem
    .user
      height .5rem
      display flex
      align-items center
      .city-name
        font-size .3rem
        font-weight: bold
      .city-img
        height .3rem
    .search
      width 5.24rem
      height .62rem
      position relative
      .search-input
        width 5.24rem
        height .62rem
        border-radius .3rem
        box-sizing border-box
        padding .1rem .4rem
        padding-left .6rem
      .search-img
        position absolute
        height .3rem
        top .16rem
        left .1rem

</style>
