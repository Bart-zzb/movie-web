<template>
  <div class="common-layout">
    <el-container>
      <!-- 首页共有头部 -->

      <el-header style="height: 132px; padding: 0;">
        <!-- 首页头部顶行-->
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
        <!-- 首页头部第二行-->
        <div style="background-color: #F0F3F5;">
          <el-row :gutter="10" style="width: 1200px;margin:0 auto;">
            <el-col :span="18" >
              <span style="color:#258DCD;font-size: 35px;margin: 50px 100px 50px 50px;line-height:70px;" >豆豆电影</span>
              <el-input placeholder="搜索电影、电视剧、综艺、影人" style="width: 500px;margin-bottom:12px;">
                <template #append>
                  <el-button :icon="Search"></el-button>
                </template>
              </el-input>
              <el-menu mode="horizontal" style="background-color: #F0F3F5;height:34px; margin: 20px auto 0px;">
                <el-menu-item style="margin-left:35px;">影讯&购票</el-menu-item>
                <el-menu-item>选电影</el-menu-item>
                <el-menu-item>电视剧</el-menu-item>
                <el-menu-item>排行榜</el-menu-item>
                <el-menu-item>影评</el-menu-item>
                <el-menu-item>2023年度榜单</el-menu-item>
                <el-menu-item>2023年度报告</el-menu-item>
              </el-menu>
            </el-col>
            <el-col :span="6">
              <img src="/imgs/annual_2023.png" style="height:120px; ">
            </el-col>
          </el-row>
        </div>
      </el-header>

      <el-main><router-view/></el-main>

      <!--首页共有页尾-->
      <el-footer style="height: 28px; padding: 0;background-color:#fff;">
        <div class="header-div">
          <span style="margin:0 10px;text-decoration: none;color: #fff;line-height: 28px;font-weight: lighter;">
            © 2000－2024 doudou.com, all rights reserved 北京豆豆科技有限公司
          </span>
          <span style="margin-left: 200px;color: #fff;line-height: 28px;font-weight: lighter;">2311 佛山祖庙中心 招泽标</span>
          <span style="position:absolute;right:0;">
            <a href="/" class="header-div-a">关于豆豆</a>|
            <a href="/" class="header-div-a">在豆瓣工作</a>|
            <a href="/" class="header-div-a">联系我们</a>|
            <a href="/" class="header-div-a">法律声明</a>|
            <a href="/" class="header-div-a">帮助中心</a>|
            <a href="/" class="header-div-a">移动应用</a>|
            <a href="/" class="header-div-a">豆瓣广告</a>
          </span>
        </div>
      </el-footer>
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