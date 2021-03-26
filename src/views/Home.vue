<template>
  <div class="denglu">
    <img src="../assets/logo.png">
    <div>
      <p>
        欢迎使用租赁平台管理系统
      </p>
  <!--    有关输入-->
      <el-row type="flex" class="row-bg" justify="center">
        <el-col class="inline-input">
          <p style="width: 380px">
            <el-input v-model="input1" placeholder="请输入账号"></el-input>
          </p>
        </el-col>
      </el-row>

      <el-row type="flex" class="row-bg" justify="center">
        <el-col>
          <p style="width: 380px">
            <el-input placeholder="请输入密码" v-model="input2" show-password></el-input>
          </p>
        </el-col>
      </el-row>

      <el-button type="primary" @click="dialogVisible = true" >登录</el-button>
    </div>
  </div>
<!--  弹窗-->
  <el-dialog
      title="提示"
      v-model="dialogVisible"
      width="30%"
      :before-close="handleClose"
  >
    <span>是否登录？</span>
    <template #footer>
    <span class="dialog-footer">
      <el-button @click="dialogVisible = false">取 消</el-button>
      <el-button type="primary" @click="dialogVisible = false,logon()" >确 定</el-button>
    </span>
    </template>
  </el-dialog>

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
  data() {
    return {
      dialogVisible: false
    };
  },
  methods:{
    logon(){
      this.$router.push('/about');
    }
  }
})
</script>

<style>
.denglu{
  box-shadow: 0 2px 4px rgba(0, 0, 0, .12), 0 0 6px rgba(0, 0, 0, .04);
  text-align: center;
  margin: 50px auto;
  padding:10px 10px;
  width: 430px;
  background-color: white;
}
</style>
