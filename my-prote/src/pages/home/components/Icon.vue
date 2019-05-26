<template>
    <!-- <div class="icons">
        <div class="icon">
            <div class="icon-img">
                <img src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png" alt="" class="icon-content" >
            </div>
            <p class="icon-des">景点</p>
        </div>
    </div> -->


<div class="swiper-container" :options="swiperOption">
    <div class="swiper-wrapper" >
        <div class="swiper-slide" v-for="(page,index) of pages" :key="index">
            <div class="icon" v-for="item of page" :key="item.id">
                <div class="icon-img">
                    <img :src="item.imgUrl" class="icon-content" >
                </div>
                <p class="icon-des">{{item.desc}}</p>
            </div>  
        </div>
    </div>
        <div class="swiper-pagination" slot="pagination"></div>
</div>
</template>
<script>
export default {
    name:'homeicon',
    props:{
        icon:Array
    },
    data(){
        return{
            swiperOption:{
             pagination:'.swiper-pagination'
        }
    }
},
computed:{
    pages(){
        const pages=[]
        this.icon.forEach((item,index)=>{
            const page=Math.floor(index/8)
            if(!pages[page]){
                pages[page]=[]
            }
            pages[page].push(item)
        })
        return pages
    }
},
mounted(){
     new Swiper ('.swiper-container', {
    loop: true,
    // 如果需要分页器
    pagination: '.swiper-pagination',
  })        
  }
}
</script>
<style lang="stylus" scoped>
.swiper-container 
    padding-bottom: 50%;
    height: 0;
    .icon
        float:left
        width:25%
        text-align: center
        .icon-img
            display: inline-block
            width: 1.1rem
            height: 1.1rem
            .icon-content
                 width: 1.1rem
                height: 1.1rem

</style>

