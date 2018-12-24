<template>
<section class="header">
  <header-banner :colorChange = "colorChange"></header-banner>
  <header-acount></header-acount>
</section>
  
</template>

<script>
  import headerBanner from "./headerComponent/headerBanner";
  import headerAcount from "./headerComponent/headerAccount"
  export default {
    components: {
      headerBanner,
      headerAcount
    },
    props: [],
    name: 'head-component',
    data() {
      return {
        controlLicenses:false,//控制执照的隐藏与显示
        timerControl:null,
        colorChange:0,//控制字体颜色
        msg: 'this is head'
      }
    },
    methods: {
      init() {
        this.colorTimer();//字体变色
      },
      colorTimer(){ //改变字体颜色
        var self = this;
        self.timerControl = setInterval(
        function(){            
          if(self.colorChange<1){
            self.colorChange = self.colorChange +1;
          }else{
            self.colorChange = 0;
          }
        },
        600);       
      },
    },
    mounted() {
      this.init();
		},
		beforeDestroy() {
      clearInterval(self.timerControl);
    }
  }
</script>

<style lang="scss" scoped>
.header{
  
}

</style>
