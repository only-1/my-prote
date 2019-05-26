<template>
<div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list :city="cities" :hotcity=" hotCities"></city-list>
    <city-alper></city-alper>
</div>
</template>
<script>
import axios from 'axios'
import CityHeader from "./components/Header.vue"
import CitySearch from "./components/Search.vue"
import CityList from "./components/List.vue"
import CityAlper from "./components/Alper"
export default {
    name:'city',
    data(){
        return{
            cities:{},
            hotCities:[]
        }
    },
    components:{
       CityHeader,
       CitySearch,
       CityList,
      CityAlper
    },
    methods:{
        getCityInfo(){
            axios.get('api/city.json').then(this.handleGetCityInfoSucc)
        },
        handleGetCityInfoSucc(res){
            res=res.data
            if(!res.ret&&res.data){
                this.cities=res.data.cities
                this.hotCities=res.data.hotCities
            }
            console.log(res)
        }
    },
    mounted(){
        this.getCityInfo()
    }
}
</script>
<style>

</style>

