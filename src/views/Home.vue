<template>
  <div class="home">

  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  data(){
    return {
      navList:[
        {tag:'公司介绍',router:''},
        {tag:'系统介绍',router:'/system'},
        {tag:'解决方案',router:'/solution'},
        {tag:'产品介绍',router:'/product'},
        {tag:'应用领域',router:'/area'},
        {tag:'项目案例',router:'/case'},
        {tag:'安e商城',router:''},
      ]
    }
  },
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss" scoped>
  
</style>
