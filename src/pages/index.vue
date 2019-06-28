<template>
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
        <ul>
          <li><a href="#">腾讯购票</a> </li>
          <li><a href="#">选电影</a> </li>
          <li><a href="#">电视剧</a> </li>
          <li><a href="#">排行榜</a> </li>
          <li><a href="#">分类</a> </li>
          <li><a href="#">影评</a> </li>
          <li><a href="#">2018年度榜单</a> </li>
          <li><a href="#">2018影音报告</a> </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'index'
}
</script>

<style scoped>
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
