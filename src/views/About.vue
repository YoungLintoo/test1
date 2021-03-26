<template>
  <div class="about">
    <el-tabs type="border-card" style="height: 90%">
      <el-tab-pane>
        <template #label>
          <span><i class="el-icon-s-home"></i> 首页</span>
        </template>
        <subhome></subhome>
      </el-tab-pane>
      <el-tab-pane>
        <template #label>
          <span><i class="el-icon-s-order"></i> 商品申请</span>
        </template>
        <goodpage></goodpage>
      </el-tab-pane>
      <el-tab-pane>
        <template #label>
          <span><i class="el-icon-s-check"></i> 店铺申请</span>
        </template>
        <storepage></storepage>
      </el-tab-pane>
      <el-tab-pane>
        <template #label>
          <span><i class="el-icon-s-data"></i> 销售额一览</span>
        </template>
      </el-tab-pane>
    </el-tabs>
  </div>
</template>

<script>
import storepage from "@/views/storepage";
import goodpage from "@/views/goodpage";
import subhome from "@/views/subhome";
export default {
  name: 'about',
  components: {
    subhome,
    storepage,
    goodpage,
  }

};

</script>

<style>
.about{
  height: 105%;
}
</style>