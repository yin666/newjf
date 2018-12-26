<template>
  <section class="header-banner">
    <div class="row banner-row">
      <div class="left-logo">
        <div class="pic-div">
        </div>
      </div>
      <nav class="right-nav">
        <ul>
          <li :class="actived === 'home' ? 'selected':''" @click="links('home')">
            <span class="banner-chinese">
              首页
            </span>
            <span class="banner-english">
              HOME
            </span>
          </li>
          <li @mouseenter="slidedown='electric'" @mouseleave="slidedown=null">
            <span class="banner-chinese">
              彩票
            </span>
            <span class="banner-english">
              Lottery
            </span>
          </li>
          <li  @mouseenter="slidedown='fish'" @mouseleave="slidedown=null">
            <span class="banner-chinese">
              外盘
            </span>
            <span class="banner-english">
              Waipan
            </span>
          </li>
          <li @mouseenter="slidedown='chess'" @mouseleave="slidedown=null">
            <span class="banner-chinese">
              JF彩票牛牛
            </span>
            <span class="banner-english">
              JF Game
            </span>
          </li>
          <!-- <router-link tag="li" to="/realPerson" :class="actived === 'realPerson' ? 'selected':''" @mouseenter="slidedown='realPerson'" @mouseleave="slidedown=null" @click="testReal">
              <span class="banner-chinese">
                真人娱乐
              </span>
              <span class="banner-english">
                CASINO
              </span>       
          </router-link>  -->
          <li :class="actived === 'realPerson' ? 'selected':''" @mouseenter="slidedown='realPerson'" @mouseleave="slidedown=null" @click="links('realPerson')">
              <span class="banner-chinese">
                真人娱乐
              </span>
              <span class="banner-english">
                CASINO
              </span>       
          </li>
          <li @mouseenter="slidedown='lottery'" @mouseleave="slidedown=null">
            <span class="banner-chinese">
              电子游艺
            </span>
            <span class="banner-english">
              Games
            </span>
          </li>
          <li @mouseenter="slidedown='promotion'" @mouseleave="slidedown=null">
            <span class="banner-chinese">
              优惠活动
            </span>
            <span class="banner-english">
              PROMOTION
            </span>
          </li>
          <li @mouseenter="slidedown='promotion'" @mouseleave="slidedown=null">
            <span class="banner-chinese">
              品牌介绍
            </span>
            <span class="banner-english">
              About US
            </span>
          </li>
          <li @mouseenter="slidedown='promotion'" @mouseleave="slidedown=null">
            <span class="banner-chinese">
              下载中心
            </span>
            <span class="banner-english">
              Download
            </span>
          </li>
        </ul>
      </nav>

    </div>
  </section>   
</template>

<script>
  export default {
    name: 'header-banne',
    props: ['colorChange'],
    data() {
      return {
        actived:"home",//  控制banner中的选中
        slidedown:null,// 控制banner中的slidedown
        msg: 'header-banne'
      }
    },
    methods: {
      links(context){ //点击导航跳转到不同页面
        switch(context) {
          case 'home':         
            this.actived = 'home';
            this.$router.push({name:'home'});
            break;
          case 'realPerson':
            this.actived = 'realPerson';
            this.$router.push('realPerson');
            break;
          default:
            // code block
        }
      },
      init() {
        console.log(this.colorChange);
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
 .header-banner{
    width:100%;
    background-image: linear-gradient(to right,#d42020 , #db3333); 
    border-bottom: 1px solid #2c281f;
    .banner-row{
      display:flex;
      justify-content: space-between;
      color:#fff;
      align-items: center;
      .left-logo{
        position:relative;
        .pic-div{
          position: relative;
          display: inline-block;
          width: 1.94rem;
          height: 0.57rem;
          vertical-align: top;
          background: url(../../../assets/img/logo194_57.png) no-repeat center center;        
        }
      }
      .right-nav{
        display:flex;
        align-items: center;
        height: 0.57rem;
        ul{
          display:flex;
          align-items: center;
          height: 100%;
          >li{
            display:flex;
            flex-direction: column;
            padding: 0 0.1rem;
            cursor: pointer;
            height: 100%;
            position:relative;
            align-items: center;
            &:hover{
              background-image: linear-gradient(to bottom,#f6e7e7 , #f17777); 
              color:#d92c2c;
            }
            .subnav {
              // display: none;
              position: absolute;
              top:103px;
              width: 130px;
              z-index: 99;
              text-align: left;
              border: 2px solid #e9dc86;
              background: rgba(0,0,0,.7);
              transition-property: all;
              transition-duration: .8s;
              transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
              transform-origin: left top;
              &:before{
                position: absolute;
                content: "";
                width: 0;
                height: 0;
                border-left: 5px solid transparent;
                border-right: 5px solid transparent;
                border-bottom: 8px solid #e9dc86;
                left: 50%;
                top: -8px
              } 
              i{ 
                position: absolute;
                width: 17px;
                height: 17px;
                right: 0px;
                top:0px;
                background:url('https://cdn.igsttech.com/Web.Portal/DQ004-01.Portal/Content/Views/Shared/images/sub_hot.gif') no-repeat center center;
              }            
            }
            .height-0{
              transform: scaleY(0);              
              overflow: hidden;              
            }
            .fish{
              left: -113px;;
              width:304px;
            }
          }
          .selected{
            background-image: linear-gradient(to bottom,#f6e7e7 , #f17777); 
            color:#d92c2c;
          }
        }
      }
    }
    .banner-chinese{
      display: inline-flex;
      box-sizing: border-box;
      padding-top: 0.1rem;
      padding-bottom:0.05rem;
    }
 }
</style>
