<template>
    <div>
        <div class="search">
        <input type="text" placeholder="请输入城市名" class="search-input" v-model="keyword">
        </div>
        <div class="search-contet" ref="search" v-show="keyword">
            <ul>
                <li v-for="item of list" class="search-item">{{item.name}}</li>
                <li v-show="hasNoData">没有找到匹配数据</li>
            </ul>
        </div>
    </div>
</template>
<script>
    import Bscroll from 'better-scroll'
export default {
    name:'citysearch',
    props:{
        city:Object
    },
    data(){
        return{
            keyword:'',
            list:[],
            timer:null
        }
    },
    computed:{
        hasNoData(){
            return !this.list.length
        }
    },
    watch:{
        keyword(){
            if(this.timer){
                clearTimeout(this.timer)
            }
            if(!this.keyword){
                this.list=[]
            }
            this.timer = setTimeout(()=>{
                const result = []
                for(let i in this.cities) {
                    this.cities[i].forEach((value)  => {
                        if(value.spell.indexOf(this.keyword)>-1 ||value.name.indexOf(this.keyword)>-1){
                            result.push(value)
                        }
                    })
                }
                this.list=result
            },100)
        }
        },
        mounted () {
            this.scroll = new Bscroll(this.$refs.search)
        }
    }

</script>
<style lang="stylus" scoped>
    .search
        height:.72rem
        padding:0 .1rem
        background:blue
        .search-input
            width:100%
            height:0.62rem
            line-height:0.62rem
            text-align:center
            border-radius:.06rem
            color:#000
    .search-content
        /*overflow:hidden
        position:absolute
        top:1.58rem
        left:0
        right:0
        background:red
        z-index:1*/
        background:red

</style>


