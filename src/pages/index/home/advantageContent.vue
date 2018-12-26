<template>
  <section class="advantage-content">
    <div class="row content">
      <ul class="advantage-ul">
        <li class="li-one">
          <div>
            <span class="size-36">0.3</span>
            <span class="size-18">秒</span>
          </div>
          <div class="middle-img">
            <img src="../../../assets/img/chart-long-bar.png" alt="">
          </div>
          <div>
            存款到账
          </div>
        </li>
        <li class="li-two">
          <div>
            <span class="size-36">25</span>
            <span class="size-18">秒</span>
          </div>
          <div class="middle-img">
            <img src="../../../assets/img/chart-short-bar.png" alt="">
          </div>
          <div>
            提款到账
          </div>
        </li>
        <li class="li-three">
          <div class="li-three-out">
            <div class="size-52">
              28
            </div>
            <div class="right-two-lines">
              <div class="size-20">
                家合作银行
              </div>
              <div class="size-14">
                提供安全资金保障
              </div>
            </div>
          </div>            
        </li>
        <li class="li-four">
          <table>
            <tr>
              <td>
                <img src="../../../assets/img/bank-icon (1).png" alt="">
              </td>
              <td>
                <img src="../../../assets/img/bank-icon (2).png" alt="">
              </td>
              <td>
                <img src="../../../assets/img/bank-icon (3).png" alt="">
              </td>
              <td>
                <img src="../../../assets/img/bank-icon (4).png" alt="">
              </td>
              <td>
                <img src="../../../assets/img/bank-icon (5).png" alt="">
              </td>
              <td>
                <img src="../../../assets/img/bank-icon (6).png" alt="">
              </td>
            </tr>
            <tr>
              <td>
                <img src="../../../assets/img/bank-icon (7).png" alt="">
              </td>
              <td>
                <img src="../../../assets/img/bank-icon (8).png" alt="">
              </td>
              <td>
                <img src="../../../assets/img/bank-icon (9).png" alt="">
              </td>
              <td>
                <img src="../../../assets/img/bank-icon (10).png" alt="">
              </td>
              <td>
                <img src="../../../assets/img/bank-icon (11).png" alt="">
              </td>
              <td>
                <img src="../../../assets/img/bank-icon (12).png" alt="">
              </td>
            </tr>
          </table>
        </li>
      </ul>
    </div>
  </section>   
</template>

<script>
  export default {
    name: 'advantage-content',
    props: [],
    data() {
      return {
        msg: 'advantage-content'
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
.advantage-content{
  position:relative;
  width: 100%;
  .content{
    display: flex;
  }
  .advantage-ul{
    width: 100%;
    display:flex;
    padding:0.4rem 0 0.4rem 0;
    justify-content: space-between;
    >li{
      color: #a7a6a6;
      text-align: center;
      position:relative;
    }
  }
  .size-36{
    font-size:0.36rem;
    color:#b0b0b0;
  }
  .size-18{
    font-size:0.18rem;
    color: #a7a6a6;
  }
  .middle-img{
    padding:0.06rem 0 0.06rem 0;
  }
  .li-one{
    flex-grow: 3;
    flex-shrink: 1;
  }
  .li-two{
    flex-grow: 3;
    flex-shrink: 1;
  }
  .li-three{
    display: flex;
    justify-content: center;
    flex-grow: 6;
    flex-shrink: 1;
    .li-three-out{
      width: 1.76rem;
      display: flex;
    }  
  }
  .li-four{
    display:flex;
    flex-grow: 2;
    flex-shrink: 1;
    align-items: center;
    justify-content: center;
    table{
      border-collapse: collapse;
    }
    td{
      padding:0.02rem;
      border: 1px solid #393536;
      img{
        vertical-align: middle;
      }
    }
  }
  .size-52{
    font-size:0.52rem;
    line-height: 0.87rem;
  }
  .right-two-lines{
    display:flex;
    flex-direction: column;
    text-align: center;
    justify-content: center;
  }
  .size-20{
    font-size: 0.2rem;
  }
  .size-14{
    font-size:0.14rem;
  }
  
}
</style>
