<template>
    <div>
        <DetailBannar></DetailBannar>
        <DetailHeader></DetailHeader>
        <DetailList :list="list"></DetailList>
        <div class="content"></div>
    </div>
</template>

<script>
import DetailBannar from './banner'
import DetailHeader from './header'
import DetailList from './list'
export default {
    name: 'Detail',
    components: {
        DetailBannar,
        DetailHeader,
        DetailList
    },
    data () {
        return {
            list: [{
                title: '成人票',
                children: [{
                    title: '成人三馆连票'
                },{
                    title: '成人五馆连票'
                }]
            },{
                title: '学生票'
            },{
                title: '儿童票'
            },{
                title: '特惠票'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
.content{
    height: 50rem
    background: #eee
}
</style>