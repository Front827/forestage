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
  <!-- 渲染样式 -->
  <div class="regi-top-div">
    <div>
      <img
        style="
          width: 50px;
          margin-left: 20px;

          border-radius: 50%;
        "
        src="../assets/logo.jpg"
        alt=""
      />
    </div>

    <div>
      <div>
        <span style="font-size: 20px; font-weight: 700; margin-right: 20px"
          >小明</span
        >

        <!-- 此处改为动态获取，title -->
        <span>主任医师</span>
      </div>
      <div>
        <span>就诊科室:</span>
        <!-- 此处改为动态获取，暂无 -->
        <span>精神心理</span>
      </div>
    </div>
  </div>
</template>
<script setup>
import { Search } from "@element-plus/icons-vue";
</script>
<style>
.regi-top-div {
  height: 90px;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  border-bottom: 1px solid;
}
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
