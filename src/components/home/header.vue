<template>
  <div class="header">
      <div class="header-left">返回</div>
      <div class="header-input">搜索内容</div>
      <router-link to="/city">
        <div class="header-right">{{this.$store.state.city}}</div>
      </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',

}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'

.header
{
    display: flex
    height: $headerHeight
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    font-size: 40%

    .header-left{
        width: 1.5rem
        float:left
    }

    .header-input{
        flex: 1
        height: 0.5rem
        line-height: 0.5rem
        margin-top: .2rem
        margin-left: .01rem
        background: #fff
        border-radius: .1rem
        color: #ccc
    }

    .header-right{
        width: 2.24rem
        float: right
        text-align: center
        color: white
    }
}

</style>
