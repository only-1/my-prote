<template>
    <div>
        <div class="weed">周末去哪玩</div>
        <ul>
                <li class="item border-bottom" v-for="item in weekedList">
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
    data(){
        return{
            weekedList:[{
                id:'0001',
                imgUrl:"http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg",
                tit:"上海必打卡",
                desc:"中西合璧，现代和传统各有各的精彩"
            },
            {
                id:'0002',
                imgUrl:"http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg",
                tit:"上海必打卡",
                desc:"中西合璧，现代和传统各有各的精彩"
            }
            ,
            {
                id:'0002',
                imgUrl:"http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg",
                tit:"上海必打卡",
                desc:"中西合璧，现代和传统各有各的精彩"
            },
            {
                id:'0002',
                imgUrl:"http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg",
                tit:"上海必打卡",
                desc:"中西合璧，现代和传统各有各的精彩"
            }
            
            ]
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

