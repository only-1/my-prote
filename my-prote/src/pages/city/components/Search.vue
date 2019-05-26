<template>
    <div class="search">
        <input type="text" placeholder="请输入城市名" class="search-input">
    </div>
</template>
<script>
export default {
    name:'citysearch'
}
</script>
<style lang="stylus" scoped>
    .search
        height:.72rem
        padding:0 .1rem
        background:blue
        .search-input
            width:100%
            height:0.62rem
            line-height:0.62rem
            text-align:center
            border-radius:.06rem
            color:#000
</style>


