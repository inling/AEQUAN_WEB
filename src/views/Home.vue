<template>
  <div class="home">
    <el-carousel :interval="5000" :loop="true" height="450px">
      <el-carousel-item v-for="(item,i) in carouselList" :key="i">
        <img :src="item.src" alt="" style="margin-left:-400px">
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  data(){
    return {
      carouselList:[]
    }
  },
  created(){

  },
  mounted(){
    this.getCList();
  },
  methods:{
    getCList(){
      var self=this;
      this.$axios.get('http://127.0.0.1:3000/index').then(res=>{
        self.carouselList=res.data;
      })
    }
  },
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss" scoped>
  
</style>
