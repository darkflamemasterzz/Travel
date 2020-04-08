<template>
  <div class="wrapper">
    <swiper ref="mySwiper" :options="swiperOptions">
        <swiper-slide v-for="item of list" :key="item.id">
            <img class="swiper-img" :src="item.imgUrl" />
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',

  props: {
    list: Array
  },

  data(){
    return {
        swiperOptions: {
          pagination: {
            el: '.swiper-pagination',
            loop: true
          },
        }
    }
  },

  computed: {
      swiper() {
        return this.$refs.mySwiper.$swiper
      }
    },

    mounted() {
      console.log('Current Swiper instance object', this.swiper)
    }
}
</script>

<style lang="stylus" scoped>
.wrapper{
    overflow: hidden 
    width: 100%
    height: 0
    padding-bottom: 31.25%
    .swiper-img{
        width: 100%
    }
}
</style>
