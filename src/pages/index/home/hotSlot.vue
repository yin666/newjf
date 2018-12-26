<template>
  <section class="hot-slot">
    <div class="content-one">
      <div>
        <span class="slot-title">
          热门老虎机
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
        <img src="../../../assets/img/casino (1).png" alt="">
        <div class="words">
          钢铁侠3
        </div>
      </li>
      <li>
        <img src="../../../assets/img/casino (2).png" alt="">
        <div class="words">
          木乃伊迷城
        </div>
      </li>
      <li>
        <img src="../../../assets/img/casino (3).png" alt="">
        <div class="words">
          洛基传奇
        </div>
      </li>
      <li>
        <img src="../../../assets/img/casino (4).png" alt="">
        <div class="words">
          金刚
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
.hot-slot{
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
  .slot-title{
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
