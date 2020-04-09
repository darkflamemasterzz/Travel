<template>
  <div class="header">
      城市选择
      <router-link to="/">
        <div class="header-back">返回</div>
      </router-link>
  </div>
</template>

<script>
export default {
    name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'

.header
overflow hidden
    position relative
    height: $headerHeight
    line-height: $headerHeight
    text-align: center 
    color: #fff
    background: $bgColor
    font-size: .32rem

    .header-back{
        position: absolute
        top: 0
        left: .2rem
        width: .64rem
        text-align: center
        font-size: .32rem
        color: #fff
    }
</style>