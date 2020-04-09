<template>
  <div>
      <CityHeader></CityHeader>
      <CitySearch></CitySearch>
  </div>
</template>

<script>
import CityHeader from './header'
import CitySearch from './search'
export default {
    name: 'City',
    components: {
        CityHeader,
        CitySearch
    }
}
</script>

<style lang="stylus" scoped>

</style>