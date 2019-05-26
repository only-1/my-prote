<template>
    <div>
        <div class="weed">周末去哪玩</div>
        <ul>
                <li class="item border-bottom" v-for="item in week">
                    <img :src="item.imgUrl" class="item-img">
                <div class="item-info">
                    <p class="item-title">{{item.tit}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
                </li>
        </ul>  
    </div>
</template>
<script>
export default {
    name:'weeked',
    props:{
        week:Array
    },
    data(){
        return{
            
        }
    }
}
</script>
<style lang="stylus" scoped>
    .weed
        line-height:.9rem
        background:#eaeaea
        text-indent:.2rem
    .item-img
        width:100%
    .item-info
        padding:.2rem 0rem .2rem .1rem
       .item-title 
            margin-bottom:.2rem
</style>

