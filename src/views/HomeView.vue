<template>
  <div class="common-layout">
    <el-container>
      <!-- 首页头部 -->
      <el-header style="background-color: #fff;height: 80px; padding: 0;">
        <div class="header-div">
          <a href="/" class="header-div-a">豆豆</a>
          <a href="/" class="header-div-a">读书</a>
          <a href="/" class="header-div-a">电影</a>
          <a href="/" class="header-div-a">音乐</a>
          <a href="/" class="header-div-a">同城</a>
          <a href="/" class="header-div-a">小组</a>
          <a href="/" class="header-div-a">阅读</a>
          <a href="/" class="header-div-a">FM</a>
          <a href="/" class="header-div-a">时间</a>
          <a href="/" class="header-div-a">豆品</a>
          <span style="position: absolute;right:0;" >
            <a href="/" class="header-div-a">下载豆豆客户端</a>
            <a href="/" class="header-div-a">登录/注册</a>
          </span>

        </div>
      </el-header>
      <el-main>Main</el-main>
      <el-footer>Footer</el-footer>
    </el-container>
  </div>
</template>

<script setup>

</script>

<style>
.header-div{
  width:100%;
  height: 28px;
  font-size: 12px;
  background-color: #545652;
  position: relative;
}

.header-div-a {
  margin:0 10px;
  text-decoration: none;
  color: #fff;
  line-height: 28px;
  font-weight: lighter;
}
</style>