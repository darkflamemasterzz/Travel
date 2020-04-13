<template>
    <div>
        <div class="bannar" @click="handleBannarClick">
            <img class="bannar-img" src="https://imgs.qunarzz.com/p/tts7/1809/5f/e3032545a9ae0202.jpg_r_390x260x95_16346325.jpg"/>
            <div class="bannar-info">
                <div class="bannar-title">大夫山深林公园</div>
                <div class="bannar-number">39</div>
            </div>
        </div>
        <common-gallary 
            :imgs="imgs" 
            v-show="showGallary"
            @close="handleGallaryClose"
        ></common-gallary>
    </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
    name: 'DetailBanner',
    components: {
        CommonGallary
    },
    data () {
        return {

            showGallary: false,
            imgs: [
                '//imgs.qunarzz.com/p/tts0/1609/96/32fe674b30c87202.jpg_r_480x320x95_a8494fdf.jpg',
                '//imgs.qunarzz.com/p/p66/201304/17/384810d022dd28f793835fbb.jpg_256x160_6a7ec251.jpg'
            ]
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