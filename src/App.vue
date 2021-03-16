<template>
  <img src="./assets/logo.png">
  <div>
    <p>
      欢迎使用租赁平台管理系统
    </p>

    <el-row type="flex" class="row-bg" justify="center">
      <el-col :span="6">
        <p style="width: 380px">
          <el-input v-model="input1" placeholder="请输入账号"></el-input>
        </p>
      </el-col>
    </el-row>

    <el-row type="flex" class="row-bg" justify="center">
      <el-col :span="6">
        <p style="width: 380px">
          <el-input placeholder="请输入密码" v-model="input2" show-password></el-input>
        </p>
      </el-col>
    </el-row>

    <el-button type="primary" @click="showout(input1),showout(input2)">登录</el-button>

  </div>

</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent ({
  setup() {
    return {
      input1: ref(''),
      input2: ref('')
    }
  },
  methods:{
    showout:function(input){
      alert(input)
    }

  }
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background-color: #f2f6fc;
}
</style>
