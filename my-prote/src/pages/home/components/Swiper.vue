<template>
<div class="swiper-container" :options="swiperOption">
    <div class="swiper-wrapper" >
        <div class="swiper-slide" v-for="item in swiperList">
          <img :src="item.imgUrl">
        </div>
    </div>
    <div class="swiper-pagination" slot="pagination"></div>
</div>
</template>
<script>
import Swiper from 'swiper';
export default {
  name: 'Swiper',
  data () {
    return {
      swiperOption:{
       pagination:'.swiper-pagination',
      },
      swiperList:[{
        id:'001',
        imgUrl:"http://img1.qunarzz.com/qs/1808/4d/077b11817a69b102.jpg"
      },
      {
        id:'0002',
        imgUrl:"http://img1.qunarzz.com/qs/1809/f6/18a4edd3d78d1102.jpg"
      }]
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
    width:100%
    
</style>

