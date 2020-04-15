<template>
    <div>
        <DetailBannar 
            :sightName="sightName"
            :bannerImg="bannerImg"
            :bannerImgs="gallaryImgs"
        ></DetailBannar>
        <DetailHeader></DetailHeader>
        <DetailList :list="list"></DetailList>
        <div class="content"></div>
    </div>
</template>

<script>
import DetailBannar from './banner'
import DetailHeader from './header'
import DetailList from './list'
import axios from 'axios'
export default {
    name: 'Detail',
    components: {
        DetailBannar,
        DetailHeader,
        DetailList
    },
    data () {
        return {
            sightName: '',
            bannerImg: '',
            gallaryImgs: [],
            list: []
        }
    },
    methods: {
        getDetailInfo () {
            axios.get('/static/mock/detail.json',{
                params: {
                    id: this.$route.params.id
                }
            }).then(this.handleGetDetaSucc)
        },
        handleGetDetaSucc (res) {
            res = res.data
            if (res.ret && res.data) {
                const data = res.data
                this.sightName = data.sightName
                this.bannerImg = data.bannerImg
                this.gallaryImgs = data.gallaryImgs
                this.list = data.categoryList
            }
        }
    },
    mounted () {
        this.getDetailInfo()
    }
}
</script>

<style lang="stylus" scoped>
.content{
    height: 50rem
    background: #eee
}
</style>