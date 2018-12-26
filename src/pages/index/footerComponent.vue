<template>
  <section class="footer">
    <div class="content">
      <div class="row links">
        <ul>
          <li>
            <span>
              关于我们
            </span> 
          </li>
          <li>
            <span>
              优惠活动
            </span> 
          </li>
          <li>
            <span>
              条款与规则
            </span> 
          </li>
          <li>
            <span>
              博彩责任
            </span> 
          </li>
          <li>
            <span>
              免责声明
            </span> 
          </li>
          <li>
            <span>
              代理合作
            </span> 
          </li>
          <li>
            <span>
              技术帮助
            </span> 
          </li>
        </ul>
      </div>
    </div>
    <div class="content advertise-pic">
      <div class="row ">
        <img class="img-advertise" src="../../assets/img/bottom-advertise.png" alt="">
      </div>
    </div>
    <div class="content last-row">
      <div class="row">
        Coryright©2018 All Rights Reserved by JF game
      </div>
    </div>
  </section>   
</template>

<script>
  export default {
    name: 'countdown',
    data() {
      return {
        msg: 'this is countdown'
      }
    },
    methods: {
      init() {
        console.log(111);
      }
    }
  }
</script>

<style lang="scss" scoped>
.footer{
  background-color: #231f20; 
  .content{
    position:relative;
    width:100%;   
    display:flex;
  }
  .links{
    display: flex;
    height: 0.52rem;
    justify-content: center; 
    border-bottom: 1px solid #2c281f;     
    ul{
      display:flex;
      width: 8.4rem;
      align-items: center;
      justify-content: space-between;
      >li{
        color:#7e7e7e;
        font-size: 0.12rem;
        padding: 0 0.1rem;
        cursor:pointer;
        &:last-child{
          border-right: 0px;
        }
      }
    }
  }
  .advertise-pic{
    position:relative;
    background-color: #262221;
    height: 0.94rem;
    line-height: 0.94rem;
    .img-advertise{
      vertical-align: middle;
    }
  }
  .last-row{
    margin:0 auto;
    height: 0.4rem;
    color: #7e7e7e;
    font-size: 0.12rem;
    text-align: center;
    line-height: 0.4rem;
  }
}
 
</style>
