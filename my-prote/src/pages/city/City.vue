<template>
<div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list></city-list>
    <city-alper></city-alper>
</div>
</template>
<script>
import CityHeader from "./components/Header.vue"
import CitySearch from "./components/Search.vue"
import CityList from "./components/List.vue"
import CityAlper from "./components/Alper"
export default {
    name:'city',
    components:{
       CityHeader,
       CitySearch,
       CityList,
      CityAlper

    }
}
</script>
<style>

</style>

