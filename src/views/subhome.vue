<template>
<div class="subhome">
  <h2>欢迎使用VUE3.0 + ElementPlus 制作的租赁平台后台管理端</h2>

  <div>
    <p>1. 所有功能都在上方标签栏里</p>

    2. <el-button @click="jumpBack()">返回登录页</el-button>
    <p>点击返回至登录页，目前跳转靠push，即可以通过浏览器返回键返回到已登录的页面</p>
  </div>
<!--  <img alt="Vue logo" src="../assets/logo.png" />-->
  <div>大多数框架和页面设计都来自elementplus的官方网站</div>
  <div>
    <el-calendar v-model="value">
    </el-calendar>
  </div>
</div>
</template>

<script>
import { useRouter } from "vue-router";

export default {
  data(){
    return{
      value:new Date()
    }
  },
  setup() {
    const router = useRouter();

    function jumpBack() {
      router.push({
        path: "/"
      });
    }
    return{jumpBack};
  }
}
</script>

<style scoped>
.subhome{
  padding-bottom: 200px;
}
</style>