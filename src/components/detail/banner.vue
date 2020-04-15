<template>
    <div>
        <div class="bannar" @click="handleBannarClick">
            <img class="bannar-img" :src="bannerImg"/>
            <div class="bannar-info">
                <div class="bannar-title">{{this.sightName}}</div>
                <div class="bannar-number">39</div>
            </div>
        </div>
        <common-gallary 
            :imgs="bannerImgs" 
            v-show="showGallary"
            @close="handleGallaryClose"
        ></common-gallary>
    </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
    name: 'DetailBanner',
    props: {
        sightName: String,
        bannerImg: String,
        bannerImgs: Array
    },
    components: {
        CommonGallary
    },
    data () {
        return {
            showGallary: false,
        }
    },
    methods: {
        handleBannarClick () {
            this.showGallary = true
        },
        handleGallaryClose () {
            this.showGallary = false
        }
    }
}
</script>

<style lang="stylus" scoped>
.bannar{
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .bannar-img{
        width: 100%
    }
    .bannar-info{
        display: flex
        position: absolute
        left: 0
        right: 0
        bottom: 0
        line-height: .6rem
        color: #fff
        background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,0.8))
        .bannar-title{
            font-size: .32rem
            flex: 1
            padding: 0 .2rem
        }
        .bannar-number{
            padding: 0 .4rem
            height: .32rem
            line-height: .32rem
            border-radius: .2rem
            font-size: .24rem
            background: rgba(0, 0, 0, .8)
        }
    }
}
</style>