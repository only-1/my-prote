<template>
<div>
  <div class="recommend">热销推荐</div>
  <ul>
      <li class="item border-bottom" v-for="item in recommList">
              <img :src="item.imgUrl" class="item-img">
          <div class="item-info">
              <p class="item-title">{{item.tit}}</p>
              <p class="item-desc">{{item.desc}}</p>
              <button class="btn">查看详情</button>
          </div>
      </li>
</ul>  
</div>
</template>
<script>
export default {
    name:'recomm',
    data(){
        return{
            recommList:[{
                id:'0001',
                imgUrl:"http://img1.qunarzz.com/sight/p0/1904/d5/d579b03a110d75a8a3.img.jpg_200x200_740bd4c0.jpg",
                tit:"上海野生动物园",
                desc:"54162条评论"
            },{
               id:'0002',
                imgUrl:"http://img1.qunarzz.com/sight/p0/1904/d5/d579b03a110d75a8a3.img.jpg_200x200_740bd4c0.jpg",
                tit:"上海野生动物",
                desc:"54167条评论",
            }
            ,{
               id:'0002',
                imgUrl:"http://img1.qunarzz.com/sight/p0/1904/d5/d579b03a110d75a8a3.img.jpg_200x200_740bd4c0.jpg",
                tit:"上海野生动物",
                desc:"54167条评论",
            }
            ,{
               id:'0002',
                imgUrl:"http://img1.qunarzz.com/sight/p0/1904/d5/d579b03a110d75a8a3.img.jpg_200x200_740bd4c0.jpg",
                tit:"上海野生动物",
                desc:"54167条评论",
            }
            ,{
               id:'0002',
                imgUrl:"http://img1.qunarzz.com/sight/p0/1904/d5/d579b03a110d75a8a3.img.jpg_200x200_740bd4c0.jpg",
                tit:"上海野生动物",
                desc:"54167条评论",
            }
            ]
        }
    }
}
</script>
<style lang="stylus" scoped>
.recommend
    line-height:.8rem
    background:#eaeaea
    text-indent:.2rem
.item
    display:flex
    height 1.9rem
    // background:red
    .item-img
        width:1.7rem
        height:1.7rem
    .item-info
        flex:1
        padding 0.1rem
        .item-title
            font-size:.32rem
            line-height: .54rem
        .item-desc
            line-height:.53rem
            font-size:.32rem 
        .btn
            background:#ff9300
            padding:0 .1rem
            color:#fff
</style>

