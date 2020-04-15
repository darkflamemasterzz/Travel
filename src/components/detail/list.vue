<template>
    <div>
        <div class="item" v-for="(item, index) of list" :key="index">
            <div class="item-title">
                <span class="item-title-icon"></span>
                {{item.title}}
            </div>
            <div v-if="item.children" class="item-children">
                <DetailList :list="item.children"></DetailList>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'DetailList',
    props: {
        list: Array
    }
}
</script>

<style lang="stylus" scoped>
.item-title{
    line-height: .8rem
    font-size: .32rem
    padding: 0 .2rem
    border-bottom: 1px solid #eee

}
.item-children{
    padding: 0 .2rem
}
</style>