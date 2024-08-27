<template>
  <div class="container">
    <NuxtLayout name="show"> </NuxtLayout>
    <div style="text-align: center; margin-top: 10px" class="com-bar">
      <img height="40px" src="../assets/logo/logo2.png" alt="Your Image" />
      <a
        href="#"
        style="
          display: block;
          text-align: right;
          font-size: 30px;
          margin-top: 5px;
          margin-right: 10px;
        "
        ><el-icon><User /></el-icon
      ></a>
    </div>
    <div style="text-align: center; margin-top: 15px">
      <el-input
        style="border-radius: 15px; width: 85%"
        placeholder="搜症状/疾病/医生"
      />
    </div>
    <!-- 预约展示区 -->
    <div class="registion-show">
      <div
        style="
          font-size: 14px;
          display: flex;
          justify-content: space-between;
          padding: 15px;
        "
      >
        <span style="color: #848496">我的预约</span>
        <span style="color: #3fa162">联系医生</span>
      </div>
      <!-- 展示个人最近的预约 -->
      <div class="registion-latest">预约</div>
    </div>
    <!-- 导航区 -->
    <div class="navigation1"></div>
    <!-- 轮播图 -->
    <div class="picture" style="width: 90%; margin-left: 5%">
      <div class="block text-center" style="text-align: center">
        <el-carousel height="200px">
          <el-carousel-item v-for="item in imageUrl" :key="item">
            <img :src="item.url" alt="" />
          </el-carousel-item>
        </el-carousel>
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import { User, Avatar } from "@element-plus/icons-vue";

//轮播图（静态）
const imageUrl = [
  {
    url: "http://www.gengdan.cn/wp-content/uploads/2023/03/2023030921323441.jpg",
  },
  {
    url: "http://www.gengdan.cn/wp-content/uploads/2023/03/2023030921333114.jpg",
  },
  {
    url: "http://www.gengdan.cn/wp-content/uploads/2023/03/2023030921323441.jpg",
  },
  {
    url: "http://www.gengdan.cn/wp-content/uploads/2023/03/2023030921325368.jpg",
  },
];
</script>
<style scoped>
/* 预约展示区样式 */
.registion-show {
  margin-top: 5%;
  width: 90%;
  height: 15%;
  background-color: white;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  margin-left: 5%;
  border-radius: 15px;
}
.registion-latest {
  width: 90%;
  height: 50px;
  background-color: #e5e5e5;

  margin-left: 5%;
  border-radius: 15px;
}
/* 导航区样式 */
div.navigation1 {
  margin-top: 5%;
  width: 90%;
  height: 20%;
  background-color: white;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  margin-left: 5%;
  border-radius: 15px;
  margin-bottom: 10%;
}
.container {
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: #fff2e0;
}
.com-bar a {
  float: right;
  color: black; /* 设置文字颜色为浅绿色 */
  text-decoration: none;
}
/* img {
  float: left;
} */
</style>
