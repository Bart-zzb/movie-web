<!--这是首页-->
<template>
  <div style="width: 1080px;margin:30px auto;padding: 0">
    <el-row :gutter="20">
      <!--首页左侧部分-->
      <el-col :span="18">
        <el-menu mode="horizontal" style="height: 30px;margin:0 auto;">
          <span style="font-size: 20px; line-height: 30px;">正在热映</span>
          <el-menu-item index="1">正在热映全部正在热映»</el-menu-item>
          <el-menu-item index="2">即将上映»</el-menu-item>
        </el-menu>

        <el-carousel indicator-position="none" interval="5000">
          <el-carousel-item v-for="item in arr">
            <el-row :gutter="10"  >
             <el-col :span="6">
               <el-card align="center" style="padding:0;">
                 <img :src="item.imgUrl" style="width: 130px;height: 180px">
                 <p style="font-size:15px;margin: 3px auto;text-align: center">{{item.title}}</p>
                 <p style="font-size:13px;margin: 3px auto;text-align: center">{{item.score}}</p>
                 <el-button type="primary" size="small"> 选座购票</el-button>
               </el-card>
             </el-col>
            </el-row>
          </el-carousel-item>
        </el-carousel>
      </el-col>
      <!--首页右侧部分-->
      <el-col :span="6"></el-col>
    </el-row>
  </div>
</template>

<script setup>
  import {ref} from "vue";

  const arr = ref([
    {imgUrl:'/imgs/movie1.jpg',title:'开心超人之时空营救',score:'暂无评分'},
    {imgUrl:'/imgs/movie2.jpg',title:'热辣滚烫',score:'7.9'},
    {imgUrl:'/imgs/movie3.jpg',title:'第二十条',score:'7.7'},
    {imgUrl:'/imgs/movie4.jpg',title:'飞驰人生2',score:'7.7'},
    {imgUrl:'/imgs/movie5.jpg',title:'破战',score:'3.2'},
    {imgUrl:'/imgs/movie6.jpg',title:'年会不能停！',score:'8.1'},
  ]);
</script>

<style scoped>

</style>