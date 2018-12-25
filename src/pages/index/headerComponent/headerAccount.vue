<template>
  <section class="header-account">
    <div class="row header-account-row">
      <div class="left-mobile">
        <span>
          手机版
        </span>
      </div>
      <div class="account-row">
        <div class="account-div">
          <i></i>
          <input class="accout" type="text" placeholder="账户">
        </div>
        <div class="pass-div">
          <i></i>
          <input class="pass" type="password" placeholder="密码">
        </div>   
        <button class="login">
          登录
        </button>
        <button class="join-us">
          免费开户
        </button>
      </div>    
    </div>
  </section>   
</template>

<script>
  export default {
    name: 'header-account',
    props: [],
    data() {
      return {
        msg: 'header-account'
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
 .header-account{
  height: 0.45rem;
  width:100%;
  background:#111;
  border-bottom: 1px solid #2c281f;
  display:flex;
  align-items: center;
  .header-account-row{
    display:flex;
    justify-content: space-between;
    align-items: center;
  }
  .account-row{
    display:flex;
    justify-content: flex-end;
    color: #bfbfbf;
    align-items: center;
    input{
      box-sizing: border-box;
      width: 163px;
      height: 33px;
      padding-left: 5px;
      margin-right: 10px;
      color: #777;
      background-color: #020202;
      border: 1px solid #3f372a;
      border-radius: 3px;
    }
    button{
      box-sizing: border-box;
      cursor: pointer;
      padding:0 10px;
      height: 33px;
      margin: 0 4px;
      color: #fff;
      font-size: 13px;
      vertical-align: top;
      background: none;
      border: none;
      border-radius: 3px;
      transition: all .3s;
    }
    .account-div{
      position:relative;
      i{
        position: absolute;
        width: 0.25rem;
        height: 0.25rem;
        left: 0.05rem;
        top: 0.05rem;
        background: url(../../../assets/img/user25_25.png) no-repeat left center;
        background-size: 0.25rem;
      }
    }
    .pass-div{
      position:relative;
      i{
        position: absolute;
        width: 0.25rem;
        height: 0.25rem;
        left: 0.05rem;
        top: 0.05rem;
        background: url(../../../assets/img/password25_25.png) no-repeat left center;
        background-size: 0.25rem;
      }
    }
    .pass-div{
      position:relative;
    }
    .accout{
      padding-left: 33px;
      background-color: #54514c;
    }
    .pass{
      padding-left: 33px;
      background-color: #54514c;
    }
    .checkcode-div{
      position:relative;
      .yzm{
        position: absolute;
        top: 4px;
        right: 13px;
        width: auto;
        height: 27px;
      }
    }
    .login{
      color: #000;
      background-image: linear-gradient(to bottom,#e8eaaf, #b5800c); 
      min-width: 0.9rem;     
    }
    .join-us{
      color: #000;
      background-image: linear-gradient(to bottom,#e1e1e1, #767676); 
      min-width: 0.9rem;  
    }
  }
 }
</style>
