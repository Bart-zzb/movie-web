<!--这是首页-->
<template>
  <div style="width: 1080px;margin:30px auto;padding: 0">
    <el-row :gutter="20">
      <!--首页左侧部分-->
      <el-col :span="18">
        <!--首页热映轮播图 -->
        <el-menu mode="horizontal" style="height: 50px;margin:0px auto;">
          <span style="font-size: 20px; line-height: 50px;">正在热映</span>
          <el-menu-item index="1">全部正在热映»</el-menu-item>
          <el-menu-item index="2">即将上映»</el-menu-item>
        </el-menu>

        <el-carousel indicator-position="none" interval="5000">
          <el-carousel-item v-for="p in arr">
            <el-row :gutter="10" >
             <el-col :span="6" v-for="item in p">
               <el-card align="center" style="padding:0;">
                 <img :src="item.imgUrl" style="width: 130px;height: 180px">
                 <p style="font-size:15px;margin: 3px auto;text-align: center;">{{item.title}}</p>
                 <p style="font-size:13px;margin: 3px auto;text-align: center;" :style="item.style">{{item.score}}</p>
                 <el-button type="primary" size="small"> 选座购票</el-button>
               </el-card>
             </el-col>
            </el-row>
          </el-carousel-item>
        </el-carousel>

        <!-- 首页热门电影 -->
        <el-menu mode="horizontal" style="height: 50px;margin:30px auto 0;">
          <span style="font-size: 20px; line-height: 50px;">最近热门电影</span>
          <el-menu-item index="1" style="width: 75px;">热门</el-menu-item>
          <el-menu-item index="2" style="width: 75px;">最新</el-menu-item>
          <el-menu-item index="3" style="width: 75px;">豆豆高分</el-menu-item>
          <el-menu-item index="4" style="width: 75px;">冷门佳片</el-menu-item>
          <el-menu-item index="5" style="width: 75px;">华语</el-menu-item>
          <el-menu-item index="6" style="width: 75px;">欧美</el-menu-item>
          <el-menu-item index="7" style="width: 75px;">韩国</el-menu-item>
          <el-menu-item index="8" style="width: 75px;">日本</el-menu-item>
        </el-menu>
            <el-row :gutter="10" >
              <el-col :span="6" v-for="item in arr2" style="margin-bottom:4px;">
                <el-card align="center" style="padding:0;">
                  <img :src="item.imgUrl" style="width: 130px;height: 180px">
                  <p style="font-size:15px;margin: 3px auto;text-align: center;">{{item.title}}</p>
                  <p style="font-size:13px;margin: 3px auto;text-align: center;" :style="item.style">{{item.score}}</p>
                  <el-button type="primary" size="small"> 选座购票</el-button>
                </el-card>
              </el-col>
            </el-row>

        <!--首页评论区-->
        <el-menu mode="horizontal" style="height: 50px;margin:30px auto 0;">
          <span style="font-size: 20px; line-height: 50px;margin-right: 10px">最受欢迎的影评</span>
          <el-menu-item index="1" style="width: 110px;">更多热门影评»</el-menu-item>
          <el-menu-item index="2" style="width: 75px;">新片影评»</el-menu-item>
        </el-menu>
        <el-row :gutter="20" style="margin:6px auto;">
          <el-col :span="3">
            <img src="/imgs/movie1.jpg" style="width: 100%;margin-top: 10px;">
          </el-col>
          <el-col :span="21">
            <p style="font-size:20px;margin-top: 10px;margin-bottom: 8px;">来自法律从业者的评价：乌托邦式普法电影</p>
            <p style="font-size:13px;margin-top: 4px;">南拳猪蛋 评论 《第二十条》 </p>
            <p style="font-size:15px;">以下是一位来自京城的律师的评价： 昨天看了《第二十条》。感觉五位杂陈，一言难尽。首先用电影形式直接喊出了 法不让与非法 公平正义的口号，这是巨大进步。 但纵观整个电影 底层逻辑完全超现实，太梦幻。检察官...
              <a href="#" style="text-decoration: none;">(全文)</a>
            </p>

          </el-col>
        </el-row>
      </el-col>

      <!--首页右侧部分-->
      <el-col :span="6"></el-col>
    </el-row>
  </div>
</template>

<script setup>
  import {ref} from "vue";

  const arr = ref([
      [
        {imgUrl:'/imgs/movie1.jpg',title:'开心超人之时空营救',score:'暂无评分',style:'color:#000'},
        {imgUrl:'/imgs/movie2.jpg',title:'热辣滚烫',score:'7.9',style:'font-weight:bold;color:orange'},
        {imgUrl:'/imgs/movie3.jpg',title:'第二十条',score:'7.7',style:'font-weight:bold;color:orange'},
        {imgUrl:'/imgs/movie4.jpg',title:'飞驰人生2',score:'暂无评分',style:'color:#000'},
      ],
      [
        {imgUrl:'/imgs/movie5.jpg',title:'破战',score:'3.2', style:'font-weight:bold;color:orange'},
        {imgUrl:'/imgs/movie6.jpg',title:'年会不能停！',score:'8.1', style:'font-weight:bold;color:orange'},
        {imgUrl:'/imgs/movie7.jpg',title:'熊出没·逆转时空',score:'6.9', style:'font-weight:bold;color:orange'},
        {imgUrl:'/imgs/movie8.jpg',title:'金手指',score:'6.2', style:'font-weight:bold;color:orange'},
      ],
    [
      {imgUrl:'/imgs/movie9.jpg',title:'八戒之天蓬下界',score:'暂无评分',style:'color:#000'},
      {imgUrl:'/imgs/movie10.jpg',title:'非诚勿扰3',score:'5.4', style:'font-weight:bold;color:orange'},
      {imgUrl:'/imgs/movie11.jpg',title:'临时劫案',score:'6.2', style:'font-weight:bold;color:orange'},
      {imgUrl:'/imgs/movie12.jpg',title:'养蜂人',score:'6.1', style:'font-weight:bold;color:orange'},
    ]
  ]);

  const arr2 = ref([
      {imgUrl:'/imgs/movie1.jpg',title:'开心超人之时空营救',score:'暂无评分',style:'color:#000'},
      {imgUrl:'/imgs/movie2.jpg',title:'热辣滚烫',score:'7.9',style:'font-weight:bold;color:orange'},
      {imgUrl:'/imgs/movie3.jpg',title:'第二十条',score:'7.7',style:'font-weight:bold;color:orange'},
      {imgUrl:'/imgs/movie4.jpg',title:'飞驰人生2',score:'暂无评分',style:'color:#000'},
      {imgUrl:'/imgs/movie5.jpg',title:'破战',score:'3.2', style:'font-weight:bold;color:orange'},
      {imgUrl:'/imgs/movie6.jpg',title:'年会不能停！',score:'8.1', style:'font-weight:bold;color:orange'},
      {imgUrl:'/imgs/movie7.jpg',title:'熊出没·逆转时空',score:'6.9', style:'font-weight:bold;color:orange'},
      {imgUrl:'/imgs/movie8.jpg',title:'金手指',score:'6.2', style:'font-weight:bold;color:orange'}
  ]);
</script>

<style scoped>


</style>