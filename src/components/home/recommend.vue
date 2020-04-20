<template>
    <div>
        <div class="recommend-title">热销推荐</div>
        <ul>
            <router-link 
                tag="li"
                :to="'/detail/' + item.id"
                class="item" 
                v-for="item of list" 
                :key="item.id"
            >
                <img class="item-img" :src='item.imgUrl' />
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </router-link>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'HomeRecommend',
    props: {
        list: Array
    },
    data () {
        return {
            
        }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'

.recommend-title{
    margin-top: .2rem
    line-height : .8rem
    background: #eee
    text-indent: .2rem
    font-size: 0.3rem
    font-weight: 500
}
.item{
    overflow hidden
    display: flex
    height: 2rem
    border-bottom: solid #eee 1px
    
    .item-img{
        width: 1.7rem
        height: 1.7rem
        padding: .1rem
        margin-top: .08rem
    }

    .item-info{
        height: 1.7rem
        flex: 1
        padding: .1rem
        margin-top: .08rem
        min-width: 0 //?
        .item-title{
            line-height: .54rem
            font-size: .4rem
            ellipsis()
            margin: .1rem .1rem
        }
        .item-desc{
            line-height: .4rem
            height: .4rem
            overflow: hidden
            text-overflow:ellipsis
            white-space:nowrap
            color: #ccc
            font-size: .3rem
            margin: .1rem
        }
        .item-button{
            line-height: .44rem
            width: 1.6rem
            // margin-top: .16rem
            background: #ff9300
            padding: 0 .1rem
            margin: .1rem
            border-radius: .06rem
            border: 1px
            color: #fff
        }
    }
}
</style>