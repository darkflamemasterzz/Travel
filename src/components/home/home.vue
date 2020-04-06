<template>
  <div>
    <HomeHeader></HomeHeader>
    <HomeSwiper></HomeSwiper>
    <HomeIcons></HomeIcons>
  </div>
</template>

<script>
import HomeHeader from './header'
import HomeSwiper from './swiper'
import HomeIcons from './Icon'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons
  }
}
</script>

<style>

</style>
