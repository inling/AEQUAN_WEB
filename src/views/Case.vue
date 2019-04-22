<template>
  <div id="case">
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
        {url:'../../img/case/6-1.png'},
        {url:'../../img/case/6-2.png'},
        {url:'../../img/case/6-3.png'},
        {url:'../../img/case/6-4.png'},
        {url:'../../img/case/6-5.png'},
        {url:'../../img/case/6-6.png'},
        {url:'../../img/case/6-7.png'},
        {url:'../../img/case/6-8.png'},
        {url:'../../img/case/6-9.png'},
        {url:'../../img/case/6-10.png'},
        {url:'../../img/case/6-11.png'},
        {url:'../../img/case/6-12.png'},
        {url:'../../img/case/6-13.png'},
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
