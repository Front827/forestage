<template>
  <div class="top-bar" style="margin-top: 15px">
    <el-icon><ArrowLeft /></el-icon>
    <span style="margin-left: 40%">眼科</span>
  </div>
  <div class="sec-bar">
    <el-tabs
      v-model="activeName"
      type="card"
      class="demo-tabs"
      @tab-click="handleClick"
    >
      <el-tab-pane label="8/20" name="first">
        <el-table :data="tableData" stripe style="width: 100%">
          <el-table-column width="150px">
            <template #default="scope">
              <el-image :src="scope.row.imgUrl"></el-image>
            </template>
          </el-table-column>
          <el-table-column prop="name" width="100" />
          <el-table-column width="100px">
            <template v-slot="scope">
              <!-- 预约按钮 -->
              <el-button
                plain
                @click="dialogVisible = true"
                type="primary"
                size="mini"
                >预约</el-button
              >
            </template>
          </el-table-column>
        </el-table>
      </el-tab-pane>
      <el-tab-pane label="8/21" name="second">8/21</el-tab-pane>
      <el-tab-pane label="8/22" name="third">8/22</el-tab-pane>
      <el-tab-pane label="8/23" name="fourth">8/23</el-tab-pane>
      <el-tab-pane label="8/24" name="fifth">8/24</el-tab-pane>
      <el-tab-pane label="8/25" name="fifth">8/25</el-tab-pane>
    </el-tabs>
  </div>
  <!-- 预约确认弹窗 -->
  <el-dialog v-model="dialogVisible" title="提示" width="300">
    <span>你确定要预约吗？</span>
    <template #footer>
      <div class="dialog-footer">
        <el-button @click="dialogVisible = false">取消</el-button>
        <el-button type="primary" @click="handleRegist" dialogVisible="false">
          确定
        </el-button>
      </div>
    </template>
  </el-dialog>
  <NuxtLayout name="tabbar"> </NuxtLayout>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import type { TabsPaneContext } from "element-plus";
import { ArrowLeft } from "@element-plus/icons-vue";
const dialogVisible = ref(false);
const handleRegist = () => {
  alert("预约成功");
};
const activeName = ref("first");

const handleClick = (tab: TabsPaneContext, event: Event) => {
  console.log(tab, event);
};

const tableData = [
  {
    imgUrl: "../assets/logo.jpg",
    name: "李世民",
  },
];
</script>

<style>
.demo-tabs > .el-tabs__content {
  padding: 32px;
  color: #6b778c;
  font-size: 32px;
  font-weight: 600;
}
.topbar {
  width: 100%;
  height: 30px;
  text-align: center;
}
.sec-bar {
  margin-top: 40px;
}
</style>
