<template>
  <div class="common-layout">
    <el-container>
      <!-- 首页头部 -->
      <el-header style="height: 80px; padding: 0;">
        <div class="header-div">
          <span><a href="/" class="header-div-a">豆豆</a></span>
          <span><a href="/" class="header-div-a">读书</a></span>
          <span><a href="/" class="header-div-a">电影</a></span>
          <span><a href="/" class="header-div-a">音乐</a></span>
          <span><a href="/" class="header-div-a">同城</a></span>
          <span><a href="/" class="header-div-a">小组</a></span>
          <span><a href="/" class="header-div-a">阅读</a></span>
          <span><a href="/" class="header-div-a">FM</a></span>
          <span><a href="/" class="header-div-a">时间</a></span>
          <span><a href="/" class="header-div-a">豆品</a></span>
          <span style="position:absolute;right:0;">
            <a href="/" class="header-div-a">下载豆豆客户端</a>
            <a href="/" class="header-div-a">登录/注册</a>
          </span>
        </div>
        <div style="background-color: #F0F3F5;">
          <el-row :gutter="10" style="width: 1200px;margin:0 auto;">
            <el-col :span="18">
              <span style="color:#258DCD;font-size: 30px;margin: 50px 100px 50px 50px;line-height:70px;" >豆豆电影</span>
              <el-input placeholder="搜索电影、电视剧、综艺、影人" style="width: 500px;margin-bottom:10px;">
                <template #append>
                  <el-button :icon="Search"></el-button>
                </template>
              </el-input>
            </el-col>
            <el-col :span="6">10</el-col>
          </el-row>
        </div>

      </el-header>
      <el-main>Main</el-main>
      <el-footer>Footer</el-footer>
    </el-container>
  </div>
</template>

<script setup>
import {Search} from '@element-plus/icons-vue'
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