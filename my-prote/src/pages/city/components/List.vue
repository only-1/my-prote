<template>
    <div class="list" ref="wrapper">
        <div>
            <div class="area">
                <div class="title border-topbottom">当前城市</div>
                    <div class="button-list">
                        <div class="button-wrapper">
                            <div class="button">北京</div>
                        </div>
                        <div class="button-wrapper">
                            <div class="button">北京</div>
                        </div>
                        <div class="button-wrapper">
                            <div class="button">北京</div>
                        </div>
                        <div class="button-wrapper">
                            <div class="button">北京</div>
                        </div>
                        <div class="button-wrapper">
                            <div class="button">北京</div>
                        </div> <div class="button-wrapper">
                            <div class="button">北京</div>
                        </div>
                    </div>
            </div>
                <div class="area">
                <div class="title border-topbottom">热门城市</div>
                    <div class="button-list">
                        <div class="button-wrapper" v-for="item of hotcity" :key="item.id">
                            <div class="button">{{item.name}}</div>
                        </div>
                    </div>
            </div>
                <div class="area" v-for="(item,key) of city" :key="key">
                <div class="title border-topbottom">{{key}}</div>
                <div class="item-list">
                    <div class="item border-bottom" v-for="inneritem of item" :key="inneritem.id">
                        {{inneritem.name}}
                    </div>
                </div>
            </div>
       </div>
    </div>
</template>
<script>
import Bscroll from 'better-scroll'
export default {
    props:{
        city:Object,
        hotcity:Array
    },
    name:'list',
    mounted(){
        this.scroll=new Bscroll(this.$refs.wrapper)
    }
}
</script>
<style lang="stylus" scoped>
.border-topbottom
    &:before
        border-color:#ccc
    &:after
        border-color:#ccc
.list
    position:absolute
    top:1.58rem
    left:0
    right:0
    bottom:0
    overflow:hidden
    .title
        line-height:.44rem
        background :#eee
        padding-left:.2rem
        color:#666
        font-size:.26rem
    .button-list
        padding:.1rem .6rem .1rem .1rem
        overflow:hidden
        .button-wrapper
            width:33.3% 
            float:left 
            .button
                margin:.1rem
                padding:.1rem 0
                text-align:center
                border:.02rem solid #ccc
                border-radius:.06rem
    .item-list
        .item
            line-height :.76rem
            color:#666
            padding-left:.2rem
</style>
