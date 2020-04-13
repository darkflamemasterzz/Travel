<template>
    <div>
        <DetailBannar></DetailBannar>
        <DetailHeader></DetailHeader>
        <div class="content"></div>
    </div>
</template>

<script>
import DetailBannar from './banner'
import DetailHeader from './header'
export default {
    name: 'Detail',
    components: {
        DetailBannar,
        DetailHeader
    }
}
</script>

<style lang="stylus" scoped>
.content{
    height: 50rem
    background: #eee
}
</style>