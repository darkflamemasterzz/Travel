<template>
  <div>
      <CityHeader></CityHeader>
      <CitySearch></CitySearch>
      <CityList></CityList>
  </div>
</template>

<script>
import CityHeader from './header'
import CitySearch from './search'
import CityList from './list'
export default {
    name: 'City',
    components: {
        CityHeader,
        CitySearch,
        CityList
    }
}
</script>

<style lang="stylus" scoped>

</style>