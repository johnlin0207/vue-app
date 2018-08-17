<template>
    <div class="box">
      <swiper class="swiper">
      <swiper-slide v-for="(items,index) of pages" :key="index">
        <div class="icon" v-for="item of items" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.img" alt="">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
      </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [
        {id: '0001', img: 'https://gw.alicdn.com/tps/TB1d30fPVXXXXbGXXXXXXXXXXXX-183-144.png_.webp', desc: '天猫'},
        {id: '0002', img: 'https://gw.alicdn.com/tfs/TB1lZyXcQyWBuNjy0FpXXassXXa-183-144.png?getAvatar=1_.webp', desc: '聚划算'},
        {id: '0003', img: 'https://gw.alicdn.com/tfs/TB163FbPVXXXXcKXXXXXXXXXXXX-183-144.png?getAvatar=1_.webp', desc: '天猫国际'},
        {id: '0004', img: 'https://gw.alicdn.com/tps/TB1eXc7PFXXXXb4XpXXXXXXXXXX-183-144.png?getAvatar=1_.webp', desc: '外卖'},
        {id: '0005', img: 'https://gw.alicdn.com/tps/TB1d30fPVXXXXbGXXXXXXXXXXXX-183-144.png_.webp', desc: '天猫'},
        {id: '0006', img: 'https://gw.alicdn.com/tfs/TB1lZyXcQyWBuNjy0FpXXassXXa-183-144.png?getAvatar=1_.webp', desc: '聚划算'},
        {id: '0007', img: 'https://gw.alicdn.com/tfs/TB163FbPVXXXXcKXXXXXXXXXXXX-183-144.png?getAvatar=1_.webp', desc: '天猫国际'},
        {id: '0008', img: 'https://gw.alicdn.com/tps/TB1eXc7PFXXXXb4XpXXXXXXXXXX-183-144.png?getAvatar=1_.webp', desc: '外卖'},
        {id: '0009', img: 'https://gw.alicdn.com/tps/TB1d30fPVXXXXbGXXXXXXXXXXXX-183-144.png_.webp', desc: '天猫'}
      ]
    }
  },
  computed: {
    pages () {
      let pages = []
      this.iconList.map((item, index) => {
        let page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~@styles/varibles.styl'
  @import '~@styles/mixins.styl'
  .box >>> .swiper-container
    width 100%
    height 0
    padding-bottom 50%
  .box
    .icon
      width 25%
      padding-bottom 25% //定义基于父元素宽度的百分比下内边距
      float left
      position relative
      .icon-img
        position absolute
        left 0
        top 0
        right 0
        bottom .44rem
        .icon-img-content
          width 100%
          box-sizing border-box //告诉浏览器去理解你设置的边框和内边距的值是包含在width内的,因此此时设置的padding不会增加内元素的width和height,不会戳出父元素来
          padding .2rem
      .icon-desc
        position absolute
        bottom 0
        text-align center
        line-height .44rem
        height .44rem
        color $darkTextColor
        width 100%
        ellipsis()
</style>
