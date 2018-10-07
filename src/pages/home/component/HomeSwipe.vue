<template>
  <div class="home-swiper">
        <mt-swipe :auto="4000">
          <mt-swipe-item v-for="(list,index) in swiper" :key="index">
            <img :src="list.img">
          </mt-swipe-item>
        </mt-swipe>
  </div>
</template>

<script>
export default {
  name:"HomeSwipe",
  data(){
    return{
      swiper:[
        {
          img:"/static/img/index/banner1.jpg"
        },
        {
          img:"/static/img/index/banner2.jpg"
        },
        {
          img:"/static/img/index/banner3.jpg"
        },
        {
          img:"/static/img/index/banner4.jpg"
        }
      ]
    }
  }
  
}
</script>


<style lang="stylus" scoped>
    .home-swiper
        height 6.5rem;
        margin-top 1px;
        img
            width 100%;
            height 6.5rem
</style>