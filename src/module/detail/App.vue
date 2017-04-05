<template>
  <div id="app">
    <img src="./images/logo.png">
    <div>详情内容</div>
    <a href="index.html">首页</a>
    <i class="icon icon-camera"></i>
  </div>
</template>

<script>
  import lib from '@/assets/js/lib.js'
  export default {
    name: 'app',
    data(){
      return {
        datas: [],
        page: 1,
        busy: false
      };
    },
    created:function(){
       lib.get("/user/alcohol/hasFillQuestionare",{sampleNumber:1},function (data) {
          if(!data.data){
              window.location.href="/h5/slightlydrunk/information.html?sampleNumber="+sampleNumber;
          } else {
              that.isAllShow = true;
          }
      });
    },
    methods:{

    },
    components: {
    }
  }
</script>
<style>
  #app{
    font-family:'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing:antialiased;
    -moz-osx-font-smoothing:grayscale;
    text-align:center;
    margin-top:60px;
  }
</style>
