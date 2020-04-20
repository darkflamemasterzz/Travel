<template>
  <div class="header">
      <div class="header-left iconfont">&#xe654;</div>
      <div class="header-input">搜索内容</div>
      <router-link to="/city">
        <div class="header-right">
          {{this.$store.state.city}}
          <span class="iconfont">&#xe606;</span>
        </div>
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
        padding-left: 0.2rem
        width: 1rem
        float:left
    }

    .header-input{
        flex: 1
        height: 0.7rem
        line-height: 0.7rem
        padding-left: 0.2rem
        margin-top: .09rem
        margin-left: .01rem
        font-size: 0.3rem
        background: #fff
        border-radius: .1rem
        color: #ccc
    }

    .header-right{
        width: 1.5rem
        float: right
        text-align: center
        color: white
        .iconfont{
          font-size: 0.3rem
        }
    }
}

</style>
