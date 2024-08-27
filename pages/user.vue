<template>
  <NuxtLayout name="menu">
    <!--页面主要内容-->

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
  </NuxtLayout>
  <NuxtLayout name="tabbar"> </NuxtLayout>
</template>
<script>
export default {
  data() {
    return {
      userInfo: {},
    };
  },
  mounted() {
    this.getUserInfo();
  },
  methods: {
    async getUserInfo() {},
  },
};
</script>

<style>
.top {
  margin: 5%;
  display: flex;
  align-items: center;
}
.welcome {
  margin-left: 10px;
}
</style>
