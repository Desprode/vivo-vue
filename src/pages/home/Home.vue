<template>
  <div class="Home">
    <!--头部的logo-->
    <div class="Homeheader"><i class="iconfont icon-VIVO"></i></div>
    <!--官方正品 图片-->
    <div class="official"><img src="/static/img/official.png" alt="图片" style="width: 100%;height:100%"></div>
    <!--首页轮播-->
    <Home-Swipe></Home-Swipe>
    <!--选购 配置 屏保 订制 列表-->
    <Home-List></Home-List>
    <!--爆款产品和商品列表-->
    <Home-Container :todos="todos"></Home-Container>
    <!--首页底部导航-->
    <Home-Footer></Home-Footer>
  </div>
  </div>  
</div>
    
</template>

<script>
import { mapState,mapMutations,mapGetters  } from 'vuex';
import { Swipe, SwipeItem } from 'mint-ui';
import { MessageBox } from 'mint-ui';
import HomeSwipe from './component/HomeSwipe';
import HomeList from './component/HomeList';
import HomeContainer from './component/HomeContainer'
import HomeFooter from '../../pages/footer'
import axios from 'axios';
export default {
  name:"Home",
  data(){
    return{
      todos:[]
    }
  },
  components:{
    HomeSwipe,
    HomeList,
    HomeContainer,
    HomeFooter
  },
  mounted:function(){
    this.getData()
  },
  methods:{
    getData:function(){
      var _this=this
      axios.get("/static/ceshi.json").then(function(res){
        console.log(res)
        _this.todos=res.data.data.home
      })
    }
  }
}
</script>

<style>
  .Home{
    border-bottom: 10px;
  }
  .Homeheader i{
    font-size: 0.55rem;
  }
   .Homeheader{
     position: fixed;
     width: 100%;
     top: 0;
     z-index: 1;
     height: 1.3rem;
     line-height: 1.3rem;
     font-size: 0.35rem;
     padding-left: 0.3rem;
     background: white;
   }
   .swipe{
     height: 6.5rem;
     margin-top: 1px;
   }
   .swipe img{
      width: 100%;
      height: 6.5rem;
  }
 
    .official{
      width: 100%;
      height: 0.8rem;
      background: white;
      margin-top: 1.33rem;
    }
</style>

