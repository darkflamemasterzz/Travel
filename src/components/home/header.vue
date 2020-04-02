<template>
  <div class="header">
      <div class="header-left">返回</div>
      <div class="header-input">搜索内容</div>
      <div class="header-right">城市</div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
.header
{
    display: flex
    line-height 0.86rem
    background: #00bcd4
    color: #fff
    font-size: 40%

    .header-left{
        width: 2rem
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
    }
}

</style>
