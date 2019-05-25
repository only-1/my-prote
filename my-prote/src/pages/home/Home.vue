<template>
    <div>
        <home-header></home-header>
        <home-swiper></home-swiper>
        <home-icon></home-icon>
        <home-recomm></home-recomm>
        <home-weeked></home-weeked>
    </div>
</template>
<script>
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper.vue'
import HomeIcon from './components/Icon.vue'
import HomeRecomm from './components/Recomm'
import HomeWeeked from './components/Weeked'
export default {
   name:'Home',
   components:{
       HomeHeader,
       HomeSwiper,
       HomeIcon,
       HomeRecomm,
       HomeWeeked
   }
}
</script>
<style scope>

</style>

