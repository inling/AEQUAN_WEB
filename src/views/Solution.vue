<template>
  <div id="solution">
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
        {url:'../../img/solution/3-1.png'},
        {url:'../../img/solution/3-2.png'},
        {url:'../../img/solution/3-3.png'}
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
