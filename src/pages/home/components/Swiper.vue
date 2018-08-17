<template>
  <swiper :options="swiperOption" class="swiper">
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id"><img class="swiper-img" :src='item.url' alt=""></swiper-slide>
    <!-- Optional controls -->
    <!--指示器-->
    <div class="swiper-pagination" slot="pagination"></div>
    <!--<div class="swiper-button-prev" slot="button-prev"></div>-->
    <!--<div class="swiper-button-next" slot="button-next"></div>-->
    <!--<div class="swiper-scrollbar" slot="scrollbar"></div>-->
  </swiper>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '001',
          url: '//img.alicdn.com/imgextra/i1/139/TB2ICt5oHZnBKNjSZFGXXbt3FXa_!!139-0-luban.jpg'
        },
        {
          id: '002',
          url: '//gw.alicdn.com/imgextra/i2/161/TB2acbjnYZnBKNjSZFKXXcGOVXa_!!161-0-lubanu.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .swiper >>> .swiper-pagination-bullet-active
    background: #ffffff
  .swiper
    width 100%
    height 0
    overflow hidden
    padding-bottom 31.29%
    background: #ccc
    .swiper-img
      width 100%

</style>
