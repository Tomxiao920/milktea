<template>
  <div id="demo" class="carousel" :style="{width:innerWidth+'px'}">
    <!-- 轮播图 -->
    <div class="carousel-inner" :style="{width:innerWidth+'px'}">
      <router-link to="/about">
        <img src="../../assets/images/carousel_item/carousel-1.jpg" :style="{width:innerWidth+'px'}" alt="">
      </router-link>
    </div>
    <!-- 轮播指示符 -->
    <ul class="carousel-indicators">
        <li class="active"></li>
        <li></li>
        <li></li>
        <li></li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return {
      innerWidth:window.innerWidth,
      imgs:[
        {
          src:'../../assets/images/carousel_item/carousel-1.jpg'
        },
        {
          src:'../../assets/images/carousel_item/carousel-2.jpg'
        }
      ]
    }
  },
  created(){
    window.addEventListener('resize',()=>{
      this.innerWidth=window.innerWidth;
    })
  },
}
</script>

<style scoped>
  .carousel{
    position: relative;
  }

/*重写指示符的样式*/
  .carousel-indicators{
    position: absolute;
    top: 210px;
    left: 93px;
  }
  .carousel-indicators li{
    list-style-type: none;
    width:15px;height:15px;
    background-color:#fff;
    margin-left:6px;
    margin-right:6px;
    border-radius: 50%;
    top:60px;
    float: left;
  }

</style>