<template>
  <NuxtLayout name="back">预约挂号</NuxtLayout>
  <div class="reg2-top-div">
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
  <div class="reg2-mid-div"></div>
  <div class="reg2-bottom-div">
    <div>信息填写</div>
    <!-- 就诊时间 -->

    <div>
      <label>就诊人</label>
      <input type="text" />
    </div>
    <div>
      <label>身份证号</label>
      <input type="text" />
    </div>
    <div>
      <label>手机号</label>
      <input type="text" />
    </div>
    <div>
      <label for="meeting-time">就诊时间</label>

      <input
        type="datetime-local"
        id="meeting-time"
        name="meeting-time"
        value="2024-8-28T19:30"
        min="2024-01-01T00:00"
        max="2034-01-01T00:00"
      />
    </div>
    <div>
      <textarea rows="10" cols="30">
疾病描述
</textarea
      >
    </div>
    <el-button>确认提交</el-button>
  </div>
</template>
<style scoped>
.reg2-top-div {
  height: 100px;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
}
.reg2-mid-div {
  height: 5px;
  background-color: antiquewhite;
}
</style>
