<template>
  <div class="list">
      <div class="area">
          <div class="title border-topbottom">当前城市</div>
          <div class="button-list">
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
          </div>
      </div>
      <div class="area">
          <div class="title border-topbottom">热门城市</div>
          <div class="button-list">
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
              <div class="button-wrapper">
                  <div class="button">北京</div>
              </div>
          </div>
      </div>
      <div class="area">
          <div class="title border-topbottom">A</div>
          <div class="item-list">
              <div class="item border-bottom">
                阿拉尔
              </div>
              <div class="item border-bottom">
                阿拉尔
              </div>
              <div class="item border-bottom">
                阿拉尔
              </div>
              <div class="item border-bottom">
                阿拉尔
              </div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: "CityList"
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'

.border-topbottom{
    &:before{
        border: 1px #ccc solid
    }
    &:after{
        border: 1px #ccc solid
    }
}
.border-bottom{
    &:before{
        border: 1px #ccc solid
    }
}

.title{
    line-height: .44rem
    background : #eee
    padding-left: .2rem
    color: #666
    font-size: .3rem
}

.button-list{
    overflow hidden //触发bfc
    padding: .1rem .3rem .1rem .1rem
    .button-wrapper{
        float: left
        width: 20%
        border-radius: .06rem
        background: #fff
        
        .button{
            margin: .1rem
            padding 0.1rem
            text-align: cenetr
            border: 0.02rem solid #ccc
            background: #fff
            text-align center
        }
    }
}

.item-list{
    .item{
        line-height: .76rem
        padding-left: .2rem
        color: #666
    }
    
}
</style>