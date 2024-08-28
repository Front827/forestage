<template>
  <NuxtLayout name="show"> </NuxtLayout>
  <div class="re-top-div">
    <div class="span1"></div>

    <el-input style="width: 90%" placeholder="搜索门诊、医生">
      <template #prefix>
        <el-icon class="el-input__icon"><search /></el-icon>
      </template>
    </el-input>
  </div>
  <!-- 分类 -->
</template>
<script setup>
import { Search } from "@element-plus/icons-vue";
</script>
<style>
.re-top-div {
  text-align: center;
  font-size: 26px;
  background-color: #69c98b;
  height: 70px;
}
.re-top-div .span1 {
  padding-top: 15px;
}
</style>
