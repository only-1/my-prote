<template>
    <div>
        <home-header :city="city"></home-header>
        <home-swiper :list="swiperList"></home-swiper>
        <home-icon :icon="iconList"></home-icon>
        <home-recomm :recom="recommendList"></home-recomm>
        <home-weeked :week="weekendList"></home-weeked>
    </div>
</template>
<script>
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper.vue'
import HomeIcon from './components/Icon.vue'
import HomeRecomm from './components/Recomm'
import HomeWeeked from './components/Weeked'
import axios from 'axios'
export default {
   name:'Home',
   components:{
       HomeHeader,
       HomeSwiper,
       HomeIcon,
       HomeRecomm,
       HomeWeeked
   },
   data(){
       return{
           city:'',
           swiperList:[],
           iconList:[],
           recommendList:[],
          weekendList:[]
       }
   },
   methods:{
       getHomeInfo(){
           axios.get('/api/index.json').then(this.getHomeInfoSucc)
       },
       getHomeInfoSucc(res){
           res=res.data
           if(res.ret&&res.data){
               this.city=res.data.city
               this.swiperList=res.data.swiperList
               this.iconList=res.data.iconList
               this.recommendList=res.data.recommendList
               this.weekendList=res.data.weekendList
           }
           console.log(res)
       }
   },
   mounted(){
       this.getHomeInfo()
   }
}
</script>
<style scope>

</style>

