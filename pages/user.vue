<template>
  <NuxtLayout name="show"> </NuxtLayout>

  <div class="top-div">
    <div>
      <img
        style="width: 50px; border-radius: 50%"
        src="../assets/logo.jpg"
        alt=""
      />
    </div>

    <div>
      <span style="font-size: 20px">你好，小明</span><br /><span>12345678</span>
    </div>
  </div>
  <div class="mid-div"></div>
  <!-- 个人信息模块（待做） -->
  <div class="user-message">
    <div class="l-img">
      <!-- 左侧头像 -->
      <img src="" alt="" />
    </div>
    <div>
      <!-- 个人信息（姓名） -->
    </div>
  </div>
  <div class="my">
    <!-- 收藏区域 -->
    <van-grid :column-num="3">
      <van-grid-item icon="star-o" text="收藏" />
      <van-grid-item icon="clock-o" text="问诊历史" />
      <van-grid-item icon="orders-o" text="我的挂号" />
    </van-grid>
    <!-- 信息区域 -->
    <van-cell-group>
      <van-cell title="消息通知" is-link />
      <van-cell title="用户反馈" is-link />
      <van-cell title="疾病百科" is-link />
      <van-cell title="退出登录" is-link />
    </van-cell-group>
  </div>
</template>
<style scoped>
.top-div {
  height: 100px;
}
.mid-div {
  height: 5px;
  background-color: antiquewhite;
}
.top-div {
  display: flex;
  align-items: center; /* 垂直居中 */
}

.top-div > div {
  flex: 1;
  padding: 30px;
}

.top-div img {
  width: 50px;
}
</style>
<script></script>
