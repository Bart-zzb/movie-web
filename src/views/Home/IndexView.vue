<!--这是首页版心-->
<template>
  <div style="width: 1080px;margin:30px auto;padding: 0">
    <el-row :gutter="20">
      <!--首页左侧部分-->
      <el-col :span="18">

        <!--首页热映轮播图-->
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
                 <img :src="item.imgUrl" style="height: 180px">
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

        <!--首页热门推荐-->
        <el-menu mode="horizontal" style="height: 50px;margin:30px auto;">
          <span style="font-size: 20px; line-height: 50px;">热门推荐</span>
        </el-menu>
        <el-carousel>
          <el-carousel-item v-for="item in bannerArr">
            <el-row :gutter="10">
              <el-col :span="12">
                <a href="#"><img :src="item.imgUrl" width="100%"></a>
              </el-col>
              <el-col :span="12">
                <p style="font-size: 25px;font-weight: bold;margin:50px 14px 30px 14px;"><a href="#" style="text-decoration: none;">{{item.title}}</a></p>
                <p style="font-size: 13px;margin:50px 14px 30px 14px;">{{item.content}}</p>
              </el-col>
            </el-row>
          </el-carousel-item>
        </el-carousel>

        <!--首页评论区-->
        <el-menu mode="horizontal" style="height: 50px;margin:30px auto 0;">
          <span style="font-size: 20px; line-height: 50px;margin-right: 10px">最受欢迎的影评</span>
          <el-menu-item index="1" style="width: 110px;">更多热门影评»</el-menu-item>
          <el-menu-item index="2" style="width: 75px;">新片影评»</el-menu-item>
        </el-menu>
        <el-row :gutter="20" style="margin:6px auto;" v-for="item in commentArr">
          <el-col :span="3">
            <img :src="item.imgUrl" style="width: 100%;margin-top: 10px;">
          </el-col>
          <el-col :span="21">
            <p style="font-size:20px;margin-top: 10px;margin-bottom: 8px;">{{item.title}}</p>
            <p style="font-size:13px;margin-top: 4px;">{{item.author}}</p>
            <p style="font-size:15px;">{{item.comment}}
              <a href="#" style="text-decoration: none;">(全文)</a>
            </p>
            <hr>
          </el-col>

        </el-row>

      </el-col>

      <!--首页右侧部分-->
      <el-col :span="6">
        <el-menu>
          <p style="font-size: 20px; line-height: 50px;margin:0px;">一周口碑榜</p>
          <el-menu-item index="1" style="height: 36px;">1.首尔之春</el-menu-item>
          <el-menu-item index="2" style="height: 36px;">2.机器人之梦</el-menu-item>
          <el-menu-item index="3" style="height: 36px;">3.梦之歌</el-menu-item>
          <el-menu-item index="4" style="height: 36px;">4.女气</el-menu-item>
          <el-menu-item index="5" style="height: 36px;">5.流行乐最传奇一夜</el-menu-item>
          <el-menu-item index="6" style="height: 36px;">6.农民</el-menu-item>
          <el-menu-item index="7" style="height: 36px;">7.如何拯救一名死去的朋友</el-menu-item>
          <el-menu-item index="8" style="height: 36px;">8.都是陌生人</el-menu-item>
          <el-menu-item index="9" style="height: 36px;">9.目中无人2</el-menu-item>
          <el-menu-item index="10" style="height: 36px;">10.动物王国</el-menu-item>
        </el-menu>

        <el-menu>
          <p style="font-size: 20px; line-height: 50px;margin-top:60px;">热门片单</p>
          <el-menu-item index="1" style="height: 50px;">现代战争篇</el-menu-item>
          <el-menu-item index="2" style="height: 50px;">入选IMDB250和豆瓣电影250的电影</el-menu-item>
        </el-menu>


        <p style="font-size: 20px; line-height: 50px;margin-top:60px;">合作联系</p>
        <hr>
        <p>电影合作邮箱: movie@doudou.com</p>
        <p>电视剧合作邮箱: tv@doudou.com</p>

        <p style="font-size: 20px; line-height: 50px;margin-top:60px;">关于我们</p>
        <hr>
        <el-row :gutter="10">
         <el-col :span="6" style="text-align: center">
           <img src="/imgs/icon1.png" width="40px;">
           <p style="margin-top: 5px;">微博</p>
         </el-col>
          <el-col :span="6">
            <img src="/imgs/icon2.png" width="40px;">
            <p style="margin-top: 5px;">微信</p>
          </el-col>
          <el-col :span="6">
            <img src="/imgs/icon3.png" width="40px;">
            <p style="margin-top: 5px;">瓣嘴</p>
          </el-col>
          <el-col :span="6">
            <img src="/imgs/icon4.png" width="40px;">
            <p style="margin-top: 5px;">光影club</p>
          </el-col>
        </el-row>
      </el-col>
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

  const bannerArr = ref([
    {imgUrl:'/imgs/banner1.jpg',title:'「豆瓣2023年度电影榜单」正式上线',content:'点击查看完整榜单，开启全年电影、剧集、综艺大赏。'},
    {imgUrl:'/imgs/banner2.jpg',title:'《死侍3》 首支中字预告',content:'死侍与金刚狼回归! 7月26日北美上映.'}
  ]);

  const commentArr = ref([
    {imgUrl:'/imgs/movie3.jpg',title:'来自法律从业者的评价：乌托邦式普法电影',author:'南拳猪蛋 评论 《第二十条》 ',comment:'以下是一位来自京城的律师的评价： 昨天看了《第二十条》。感觉五位杂陈，一言难尽。首先用电影形式直接喊出了 法不让与非法 公平正义的口号，这是巨大进步。 但纵观整个电影 底层逻辑完全超现实，太梦幻。检察官...'},
    {imgUrl:'/imgs/movie7.jpg',title:'豆瓣评分机制该改改了',author:'豆友3aNDCNSMLE 评论 《熊出没·逆转时空》 ',comment:'那些恶意评分的人，我不知道他们看过电影没有，如果看过了来评分的，我觉得再怎么样也不可能给他一个差评，一星两星的，可能是他（她）的童年过得并不好吧，导致他（她）对有关童年的事都很反感，这是一种心理上...'},
    {imgUrl:'/imgs/movie4.jpg',title:'飞驰人生2中的小细节',author:'你说呢  评论 《飞驰人生2》 ',comment:'按片中顺序…… 1. 驾校玻璃门原本贴着“冠军教练”，被举/报后，“冠军”没了。厉小海被卖后，“教练”没了。很心疼张驰。 2. 雨中张驰接电话“我不是张驰”似乎有模仿记星口音，加上后面翻车说是孙宇强开翻的，真是背锅二人组。 3. 老头乐的“奔驰小g”字幕是小写，比赛后的...'},
  ]);
</script>

<style scoped>


</style>