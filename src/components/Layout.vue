<template>
   <div>
     <div id="db-global-nav" class="global-nav">
       <div class="bd">
         <div class="global-nav-items">
           <ul>
             <li><a href="#">豆瓣</a> </li>
             <li><a href="#">读书</a> </li>
             <li><a href="#">电影</a> </li>
             <li><a href="#">音乐</a> </li>
             <li><a href="#">同城</a> </li>
             <li><a href="#">小组</a> </li>
             <li><a href="#">阅读</a> </li>
             <li><a href="#">FM </a> </li>
             <li><a href="#">时间</a></li>
             <li><a href="#">豆品</a> </li>
             <li><a href="#">更多</a> </li>
             <li><a href="#">读书</a> </li>
           </ul>
         </div>
         <div class="top-nav-info"><a href="#">登陆注册</a></div>
         <div class="top-nav-doubanapp"><a href="#">下载豆瓣客户端</a></div>
       </div>
     </div>
     <div class="db-nav-movie">
       <div class="nav-wrap">
         <div class="nav-primary">
           <div class="nav-logo">
             <a href="#">豆瓣电影</a>
           </div>
           <div class="nav-search">
             <div class="inp">
               <el-input
                 placeholder="搜索电影、电视剧、综艺、影人"
                 v-model="input"
                 clearable>
               </el-input>
             </div>
             <div class="inp-btn"></div>
           </div>
         </div>
       </div>
       <div class="nav-secondary">
         <div class="nav-items">
           <li><a href="#">腾讯购票</a> </li>
           <li><a href="#">选电影</a> </li>
           <li><a href="#">电视剧</a> </li>
           <li><a href="#">排行榜</a> </li>
           <li><a href="#">分类</a> </li>
           <li><a href="#">影评</a> </li>
           <li><a href="#">2018年度榜单</a> </li>
           <li><a href="#">2018影音报告</a> </li>
         </div>
       </div>
     </div>
     <div>
       <router-view></router-view>
     </div>
   </div>
</template>

<script>
export default {
  name: 'Layout'
}
</script>

<style scoped>
  body,ol,ul,h1,h2,h3,h4,h5,h6,p,th,td,dl,dd,form,fieldset,legend,input,textarea,select{margin:0;padding:0}
  body{font:12px "宋体","Arial Narrow",HELVETICA;background:#fff;-webkit-text-size-adjust:100%}
  a{color:#172c45;text-decoration:none}
  a:hover{color:#cd0200;text-decoration:underline}
  em{font-style:normal}
  li{list-style:none}
  img{border:0;vertical-align:middle}
  table{border-collapse:collapse;border-spacing:0}
  p{word-wrap:break-word}
body{
  font-size: 14px;
}
.bd{
  width: 100%;
  height: 28px;
  background: #545652;
  color: #d5d5d5;
  vertical-align: middle;
}
  .global-nav-items li {
    list-style: none;
    display: inline-block;
    padding: 0 12px;
    vertical-align: middle;
    color: #d5d5d5;
  }
  .global-nav-items{
    display: inline-block;
    vertical-align: middle;
  }
  .global-nav-items a{
    text-decoration: none;
    color: #d5d5d5;
  }
  .top-nav-doubanapp{
    display: inline-block;
    float: right;
    cursor: pointer;
    padding: 0 12px;
  }
  .top-nav-doubanapp a{
    color: #d5d5d5;
    text-decoration: none;
    vertical-align: middle;
  }
  .top-nav-info{
    display: inline-block;
    float: right;
    cursor: pointer;
    padding: 0 12px;
    vertical-align: middle;
  }
  .top-nav-info a{
    color: #d5d5d5;
    text-decoration: none;
    vertical-align: middle;
  }

  .db-nav-movie{
    background: #f0f3f5;
    position: relative;
    margin-bottom: 40px;
  }
  .nav-primary{
    width: 1040px;
    margin: 0 auto;
    height: 75px;
    display: block;
    padding: 10px 0 5px;
  }
  .nav-logo{
    height: 56px;
    width: 145px;
    display: inline-block;
    margin: auto 0;
  }
  .nav-logo a{
    color: #27a;
    text-decoration: none;
    font-size:28px;
    font-weight: bold;
  }
  .nav-search{
    display: inline-block;
  }
  .inp{
    width: 470px;
    height: 34px;
  }
  .inp el-input{
    display: inline-block;
  }
  .nav-secondary{
  }
  .nav-items{
    width: 1040px;
    height: 40px;
    margin: 0 auto;
  }
  .nav-items li {
    display: inline-block;
    text-decoration: none;
    cursor: pointer;
    list-style: none;
  }
  .nav-items li a{
    text-decoration: none;
    margin-right: 20px;
  }
</style>
