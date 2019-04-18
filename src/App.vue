<template>
  <div id="app">
    <el-container>
      <el-header class="header">
        <el-row class="logo-row">
          <el-col :span="24">
            <router-link to="/">
              <img src="./assets/img/logo.jpg" alt="">
            </router-link>
          </el-col>
        </el-row>
        <el-row>
          <el-col :span="24">
            <div class="grid-content bg-purple-dark">
              <el-row class="nav">
                <el-col v-for="(item,i) in navList" :key="i" :span="3">
                  <router-link :to="item.router" v-text="item.tag"  :class="{'nav_active':item.navActive}"></router-link>
                </el-col>
              </el-row>
            </div>
          </el-col>
        </el-row>
      </el-header>
      <el-main  class="main">
        <router-view/>
      </el-main>
      <el-footer  class="footer"></el-footer>
    </el-container>
  </div>
</template>

<script>
export default {
  data(){
    return {
      navList:[
        {tag:'公司介绍',router:'/',navActive:false},
        {tag:'系统介绍',router:'/system',navActive:false},
        {tag:'解决方案',router:'/solution',navActive:false},
        {tag:'产品介绍',router:'/product',navActive:false},
        {tag:'应用领域',router:'/area',navActive:false},
        {tag:'项目案例',router:'/case',navActive:false},
        {tag:'安e商城',router:''},
      ]
    }
  },
  created(){

  },
  mounted(){

  },
  methods:{
    crouter(){
      alert(1)
      for(var i=0;i<this.navList.length;i++){
        this.navList[i].navActive=false;
      }
      item.navActive=true;
    }
  }
}
</script>

<style lang="scss">
  .header,.main,.footer{
    padding:0 !important;
  }
  .header{
    text-align: center;
    .logo-row{
      width:980px;
      margin:0 auto;
      text-align:left;
      .el-col{
        margin-top:8px;
      }
    }
    .nav{
      width:980px;
      height:100%;
      line-height: 35px;
      margin:0 auto;
      .el-col{
        cursor: pointer;
        a{
          display: inline-block;
          width:100%;
          height:100%;
          color:white;
          font-size: 14px;
          &:hover{
            background:#616369;
          }
        }
      }
    }
  }

  .nav_active{
    background:#D9070A;
  }
</style>
