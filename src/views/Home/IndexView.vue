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
          <el-carousel-item >
            <el-row :gutter="10" >
             <el-col :span="6" v-for="item in arr">
               <el-card align="center">
                 <img :src="arr.imgUrl" style="width: 130px;">
                 <p style="font-size:15px;margin: 3px auto;text-align: center">{{arr.title}}</p>
                 <p style="font-size:13px;margin: 3px auto;text-align: center">{{arr.score}}</p>
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
    {imgUrl:'/imgs/movie2.jpg',title:'开心超人之时空营救',score:'暂无评分'},
  ]);
</script>

<style scoped>

</style>