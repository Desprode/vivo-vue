<template>
  <div class="Author" >
      <div class="AuthorHeader">
        <router-link to="my">
          <i class="iconfont icon-552cc14536532"></i>
        </router-link>
          关于我
      </div>
  </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
}
</script>

<style>
.Author{
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 999;
  background: white;
}
.AuthorHeader{
    position: fixed;
    top: 0;
    width: 100%;
    height: 1.3rem;
    line-height: 1.3rem;
    background: white;
    padding-left: 0.3rem;
    -webkit-box-shadow: 0 0 10px #cecece;
    box-shadow: 0 0 10px #cecece;
    z-index: 1;
    font-size: 0.41rem;
}
.AuthorHeader i{
    display: block;
    float: left;
    height: 50px;
    font-size: 0.71rem;
    color: black;
    width: 0.9rem;
}

</style>
