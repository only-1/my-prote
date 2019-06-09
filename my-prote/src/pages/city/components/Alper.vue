<template>
    <ul class="list">
        <li class="item" v-for="(item,key) of letters" :key="item" :ref="key" @click="handletterClick" @touchstart="handleTouchStart">{{item}}</li>
    </ul>
</template>
<script>
export default {
    name:'alper',
    computed:{
letters(){
    const letters=[]
    for(let i in this.city){

    }
}
    },
    data(){
return{
    touchStatus:false
}
    },
    props:{
        city:Object
    },
    methods:{
        handletterClick(e){
            this.$emit('change',e.target.innertext)
            console.log(e.target.innertext)
        },
        handletterClick(e){
            this.touchStatus=true
        }       
}
}
</script>
<style lang="stylus" scoped>
    .list
        display:flex
        flex-direction:column
        position:absolute
        top:1.58rem
        right:0
        bottom:0
        width:.4rem
        justify-content: center;
        .item
            text-align:center
            line-height:.42rem
</style>
