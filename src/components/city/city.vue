<template>
  <div>
      <CityHeader></CityHeader>
      <CitySearch></CitySearch>
      <CityList></CityList>
      <CityAlphabet></CityAlphabet>
  </div>
</template>

<script>
import CityHeader from './header'
import CitySearch from './search'
import CityList from './list'
import CityAlphabet from './alphabet'
export default {
    name: 'City',
    components: {
        CityHeader,
        CitySearch,
        CityList,
        CityAlphabet
    }
}
</script>

<style lang="stylus" scoped>

</style>