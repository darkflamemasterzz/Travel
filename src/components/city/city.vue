<template>
  <div>
      <CityHeader></CityHeader>
      <CitySearch></CitySearch>
      <CityList :cities="cities" :hot="hotCities"></CityList>
      <CityAlphabet :cities="cities"></CityAlphabet>
  </div>
</template>

<script>
import axios from 'axios'
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
    },
    data () {
        return {
            cities: {},
            hotCities: []
        }
    },
    methods: {
        getCityInfo () {
            axios.get('/static/mock/city.json')
                .then(this.handleGetCityInfoSucc)
        },
        handleGetCityInfoSucc (res) {
            res = res.data
            if (res.ret && res.data){
                const data = res.data
                this.cities = data.cities
                this.hotCities = data.hotCities
            }
        }
    },
    mounted () {
        this.getCityInfo()
    }
}
</script>

<style lang="stylus" scoped>

</style>