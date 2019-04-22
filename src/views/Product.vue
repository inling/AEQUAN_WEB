<template>
  <div id="product">
    <el-carousel :interval="5000" :loop="true" height="450px">
      <el-carousel-item v-for="(item,i) in carouselList" :key="i">
        <img :src="item.url" alt="" style="margin-left:-400px">
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
export default {
  data(){
    return {
      carouselList:[
        {url:'../../img/product/4-1.png'},
        {url:'../../img/product/4-2.png'},
        {url:'../../img/product/4-3.png'},
        {url:'../../img/product/4-4.png'},
        {url:'../../img/product/4-5.png'},
        {url:'../../img/product/4-6.png'},
        {url:'../../img/product/4-7.png'},
        {url:'../../img/product/4-8.png'},
        {url:'../../img/product/4-9.png'},
        {url:'../../img/product/4-10.png'}
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  .el-carousel{
    border-bottom: 1px solid #d4d4d4;
    box-shadow: 0px 1px 48px #d4d4d4;
  }
</style>
