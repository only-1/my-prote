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
    data(){
        return{
            swiperOption:{
             pagination:'.swiper-pagination'
        },
        iconList:[{
            id:'0001',
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
            desc:'景点'
        },{
          id:'0002',
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png",
            desc:'一日游'  
        }
        ,{
          id:'0003',
            imgUrl:"http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/3ef092d0a89ffddb7f781cda30c8ae49.png",
            desc:'上海'  
        }
        ,{
          id:'0004',
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/f5/c4c9d9830404e602.png",
            desc:'室内娱乐'  
        }
        ,{
          id:'0005',
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png",
            desc:'动植物园'  
        }
        ,{
          id:'0006',
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png",
            desc:'世纪公园'  
        }
        ,{
          id:'0007',
            imgUrl:"http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/cb506456115da181cd1deadfa17bfee9.png",
            desc:'浦江郊野公园'  
        },
        {
          id:'0008',
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png",
            desc:'上海野生'  
        }
        ,
        {
          id:'0009',
            imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/de/f26be47a6bf02a02.png",
            desc:'上海迪士尼'  
        }
        ]
    }
},
computed:{
    pages(){
        const pages=[]
        this.iconList.forEach((item,index)=>{
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

