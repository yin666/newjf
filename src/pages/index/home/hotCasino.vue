<template>
  <section class="hot-casino">
    <div class="content-one">
      <div>
        <span class="casino-title">
          热门娱乐场
        </span>
      </div>
      <div>
        <button class="more-g-btn">
          更多游戏
        </button>
      </div>
    </div>
    <ul class="content-two">
      
      <li>
        <img src="../../../assets/img/realperson (2).png" alt="">
        <div class="words">
          AG娱乐
        </div>
      </li>
      <li>
        <img src="../../../assets/img/realperson (3).png" alt="">
        <div class="words">
          OG娱乐
        </div>
      </li>
      <li>
        <img src="../../../assets/img/realperson (4).png" alt="">
        <div class="words">
          EBET娱乐
        </div>
      </li>
      <li>
        <img src="../../../assets/img/realperson (1).png" alt="">
        <div class="words">
          JF娱乐
        </div>
      </li>
    </ul>
  </section>   
</template>

<script>
  export default {
    name: 'more-games',
    props: [],
    data() {
      return {
        msg: 'more-games'
      }
    },
    methods: {
      init() {
      }
    },
    mounted() {
      this.init();
		},
		beforeDestroy() {
    }
  }
</script>

<style lang="scss" scoped>
.hot-casino{
  position:relative;
  width: 5.56rem;
  .content-one{
    width: 100%;
    margin-top:0.1rem;
    display:flex;
    justify-content: space-between;
    border-bottom: 1px solid #393536;
    padding: 0.1rem 0;
  }
  .casino-title{
     color:#ddd595;
     font-size: 0.22rem;
  }
  .more-g-btn{
    @extend %btn-yellow;
  }
  .content-two{
    margin-top:0.1rem;
    display:flex;
    justify-content: space-around;
    li{
      cursor: pointer;
    }
  }
  .words{
    text-align: center;
    color: #a4a4a4;
    font-size: 0.14rem;
    margin-top: 0.1rem;
  }
}
</style>
