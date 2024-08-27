<template>
  <div class="top-div">
    <div class="span1">
      <span>预约挂号</span>
    </div>
    <br />

    <el-input style="width: 90%" placeholder="搜索门诊、医生">
      <template #prefix>
        <el-icon class="el-input__icon"><search /></el-icon>
      </template>
    </el-input>
  </div>
  <!-- 分类 -->

  <el-menu style="width: 200px; height: calc(100vh - 50px)" :default-active="2">
    <el-menu-item index="1-4-1" @Click="onChoose">眼科</el-menu-item>
    <el-menu-item index="1-4-2">儿科</el-menu-item>
    <el-menu-item index="1-4-3">内科</el-menu-item>
    <el-menu-item index="1-4-4">外科</el-menu-item>
  </el-menu>

  <NuxtLayout name="tabbar"> </NuxtLayout>
</template>
<script setup>
const onChoose = () => {
  navigateTo("/reg2", { replace: true });
};
</script>
<style>
.top-div {
  text-align: center;
  font-size: 26px;
  background-color: #69c98b;
  height: 150px;
}
.top-div .span1 {
  padding-top: 15px;
}
</style>
