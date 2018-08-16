<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont">&#xe600;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe617;</span>
      输入城市/景点/游玩主题</div>
    <div class="header-right">城市
      <span class="iconfont">&#xe6b5;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home-header'
}
</script>

<style lang="stylus" scoped>
  @import '~@styles/varibles.styl'
  .header
    height .86rem//(设置的1px在Retina上显示2px),43px对应(50px=1rem的)0.86rem
    display flex
    line-height .86rem
    background $bgColor
    align-items center
    .header-left
      width .64rem;
      text-align center
    .header-right
      width 1.24rem
      text-align center
    .header-input
      flex:1
      background #fff
      border-radius .1rem
      height .64rem
      display flex
      align-items center
      margin-left .2rem
      padding-left .1rem
</style>
