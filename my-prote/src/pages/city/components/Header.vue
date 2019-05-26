<template>
  
        <div class="header">
            城市选择
           <router-link to='/'>
                <div class="iconfont header-icon">&#xe624;</div>
            </router-link>
        </div>
  
</template>
<script>
export default {
    name:'header'
}
</script>
<style lang="stylus" scoped>
.header
    text-align:center
    height:.86rem
    line-height:0.86rem
    background:red
    position relative
    .header-icon
        width:0.84rem
        position:absolute
        top:0

</style>
