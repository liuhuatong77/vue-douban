<template>
    <div id="wrapper">
      <div class="content">
        <div class="grid-16-8-clearfix">
          <div class="conten-left">
            <div class="conten-left-left">
              <div class="screening-hd">
                <div class="hd-left">
                  <div class="hd-text">
                    正在热映 <span>全部正在热映>></span><span>即将上映</span>
                  </div>
                </div>
                <div class="hd-right">
                  <div class="hd-page">
                    1/7
                  </div>
                  <div class="hd-next">
                    左右
                  </div>
                </div>
              </div>
              <div class="screeing-bd">
                <slide-show :slides="HotLists"></slide-show>
              </div>
            </div>
          </div>
          <div class="conten-right">
            <div class="conten-right-right">
              <div class="right-hd">
                <div class="right-hd-text" ><span>豆瓣电影评分8问</span></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import slideShow from './slideShow'

export default {
  name: 'wrapper',
  data () {
    return {
      HotLists: []
    }
  },
  components: {
    slideShow
  },
  created: function () {
    // this.$axios.get('api').then((response) => {
    //   this.HotLists = response.data
    //   console.log(response.data)
    // })
    this.$axios.get('api/v2/movie/in_theaters?start=0&count=5').then(response => {
      this.HotLists = response.data.subjects
      console.log(response.data)
    }).catch(error => {
      console.log(error)
    })
  }
}
</script>

<style scoped>
  .grid-16-8-clearfix{
    width: 1040px;
    margin: 0 auto;
  }
  .conten-left{
    width: 675px;
    padding-right: 40px;
    float: left;
  }
.hd-left{
  display: inline-block;
  float: left;
}
  .hd-right{
    display: inline-block;
    float: right;
  }
  .hd-page{
    display: inline-block;
  }
.hd-next{
  display: inline-block;
}
  .conten-right{
    width: 300px;
    float: right;
  }
  .screening-hd{
    height: 30px;
    border-bottom: 1px solid #eee;
  }
</style>
