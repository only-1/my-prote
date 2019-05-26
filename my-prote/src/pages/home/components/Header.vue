<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-icon">&#xe624;</div>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe632;</span>
            输入城市景点</div>
        <div class="header-right">{{this.city}}
            <span class="iconfont icon-font">&#xe64a;</span>
        </div>
    </div>
</template>
<script>
export default {
   name:'HomeHeader',
   props:{city:String}
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header
    display: flex
    line-height: 0.86rem
    background: $bgColor
    color:#fff

    .header-left
        width: 0.64rem
        float:left
        .back-icon
            font-size:.4rem
            text-align:center
    .header-input
        flex:1
        height 0.64rem
        line-height .64rem
        background:#fff
        border radius 0.1rem
        margin-top:.12rem
        margin-left:0.2rem
        padding-left: .2rem;
        color:black
    .header-right
        width:1.24rem
        float:right
        text-align:center
        .icon-font
            font-size: .2rem

</style>

