<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title" v-text="item.title"></p>
          <p class="item-desc" v-text="item.desc"></p>
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
      recommendList: [{
        id: '001',
        imgUrl: 'http://gw.alicdn.com/imgextra/TB2oHQ5XgHqK1RjSZFgXXa7JXXa_!!10-0-lubanu.jpg',
        title: '魔力电动车',
        desc: '这是一款魔力电动车'
      }, {
        id: '002',
        imgUrl: 'http://gw.alicdn.com/imgextra/TB2oHQ5XgHqK1RjSZFgXXa7JXXa_!!10-0-lubanu.jpg',
        title: '魔力电动车',
        desc: '这是一款魔力电动车'
      }, {
        id: '003',
        imgUrl: 'http://gw.alicdn.com/imgextra/TB2oHQ5XgHqK1RjSZFgXXa7JXXa_!!10-0-lubanu.jpg',
        title: '魔力电动车',
        desc: '这是一款魔力电动车'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@styles/mixins.styl'
  .recommend-title
    line-height .8rem
    background #eee
    text-indent .2rem
    margin-top .2rem
  .item
    overflow hidden
    .item-img-wrapper
      overflow hidden
      height 0
      padding-bottom 33.9%
      .item-img
        width 100%
    .item-info
      padding .1rem
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()

</style>
