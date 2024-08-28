<template>
  <div class="container">
    <NuxtLayout name="show"> </NuxtLayout>
    <div class="com-top-bar">
      <el-input style="width: 90%; margin-top: 15px" placeholder="搜索关键字">
        <template #prefix>
          <el-icon class="el-input__icon"><search /></el-icon>
        </template>
      </el-input>
      <el-row style="text-align: center; margin-top: 30px" class="top-row">
        <el-col
          :span="6"
          style="display: flex; flex-direction: column; align-items: center"
        >
          <div
            style="
              width: 65px;
              height: 65px;
              background-color: #42b983;
              border-radius: 50%;
              display: flex;
              justify-content: center;
              align-items: center;
              color: white;
              font-size: 30px;
              margin-bottom: 10px;
            "
          >
            <el-icon><Document /></el-icon>
          </div>
          <span>订单消息</span>
        </el-col>

        <el-col
          :span="6"
          style="display: flex; flex-direction: column; align-items: center"
        >
          <a :href="'/InterMessage/'">
            <div
              style="
                width: 65px;
                height: 65px;
                background-color: #ff9900;
                border-radius: 65%;
                display: flex;
                justify-content: center;
                align-items: center;
                color: white;
                font-size: 30px;
                margin-bottom: 10px;
              "
            >
              <el-icon><ChatDotRound /></el-icon>
            </div>
            <span style="color: black">互动消息</span>
          </a>
        </el-col>
        <el-col
          :span="6"
          style="display: flex; flex-direction: column; align-items: center"
          ><div
            style="
              width: 65px;
              height: 65px;
              background-color: #00b0f2;
              border-radius: 50%;
              display: flex;
              justify-content: center;
              align-items: center;
              color: white;
              font-size: 30px;
              margin-bottom: 10px;
            "
          >
            <el-icon><User /></el-icon>
          </div>
          <span>好友动态</span>
        </el-col>
        <el-col
          :span="6"
          style="display: flex; flex-direction: column; align-items: center"
          ><div
            style="
              width: 65px;
              height: 65px;
              background-color: #66cdaa;
              border-radius: 50%;
              display: flex;
              justify-content: center;
              align-items: center;
              color: white;
              font-size: 30px;
              margin-bottom: 10px;
            "
          >
            <el-icon><Bell /></el-icon>
          </div>
          <span>系统消息</span>
        </el-col>
      </el-row>
    </div>
    <div class="com-mid-bar"></div>
    <!-- 将历史消息铺开 -->
    <div class="com-bot-bar"></div>
  </div>
</template>
<script setup lang="ts">
import {
  Search,
  ChatDotRound,
  Bell,
  Document,
  User,
} from "@element-plus/icons-vue";
</script>
<style scoped>
.com-top-bar {
  height: 200px;
  text-align: center;
  background-color: white;
}
/* .top-row span {
  padding-top: 15px;
} */
.container {
  position: absolute;
  width: 100%;
  height: 100%;

  background-color: white;
}
.com-mid-bar {
  height: 10px;
  background-color: azure;
}
.com-bot-bar {
  margin-top: 10px;

  background-color: white;
}
</style>
