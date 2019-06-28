<template>
  <div class="nav-slide">
    <div class="nav-slide-list" v-for="item in slides" v-bind:key="item.id">
      <!--<div class="slide-img"><img :src="item.images.small" ></div>-->
      <div class="slide-img"><img src="https://images.weserv.nl/?url='https://img1.doubanio.com/view/photo/s_ratio_poster/public/p2557573348.jpg'" ></div>
      <div class="slide-title">{{item.title}}</div>
      <div class="slide-score-star">
        <star size=24 :score="item.rating.average"></star>
        <div class="slide-score">{{item.rating.average}}</div>
      </div>
      <div class="slide-sell">选座购票</div>
    </div>
  </div>
</template>

<script>
import star from '../components/star'

export default {
  name: 'slideShow',
  components: {
    star
  },
  props: {
    slides: {
      type: Array,
      require: true
    }
  }
}
</script>

<style scoped>
.slide-img img{
  height: 160px;
  width: 115px
}
  .nav-slide-list{
  display: inline-block;
    height: 250px;
    width: 115px;
    margin-right: 20px;
  }
  .slide-title{
    overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  }
  .slide-score{
    display: inline-block;
  }
</style>
