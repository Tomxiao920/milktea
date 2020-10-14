<template>
  <div>
      <h3>首页</h3>
      <carousel></carousel>
  </div>
</template>

<script>
//引入轮播组件对象
import carousel from "../components/Index/Carousel"
export default {
    //将carousel作为子组件
    components:{ carousel }
}
</script>

<style scoped>
    div>h3{
        text-align: center;
        margin-bottom: 10px;
    }
</style>