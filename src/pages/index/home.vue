<template>
  <section class="home">
    <div class="home-out">
    </div>
    <div class="announcement-out">
      <div class="announcement row">
        <div class="news">
          最新公告/NEWS：
        </div>
        <div class="marquee">
          <marquee ref="marquee" direction="left" loop="-1" >
            <ul>
              <li>尊敬的各位用户，我们的银联卡已经更换为工商银行，刘**名 6334783748474947 ，请留意</li>
            </ul> 
          </marquee>
        </div>
      </div>
    </div>
    <more-games></more-games>
    <div class="content-out">
      <div class="content row">
        <ul>
          <li class="two-position">
            <div class="shade">

            </div>
          </li>
          <li class="one-position">           
            <div class="img">
              <div class="shade">
                <span class="enter-game">
                  进入游戏
                </span>              
              </div>
            </div>           
            <div>
              申博太阳城，知名顶级，极度博彩
            </div>
          </li>
          <li class="one-position">
            <div class="img">
              <div class="shade">
                <span class="enter-game">
                  进入游戏
                </span>              
              </div>
            </div>
            <div>
              申博太阳城，知名顶级，极度博彩
            </div>
          </li>
          <li class="one-position">
            <div class="img">
              <div class="shade">
                <span class="enter-game">
                  进入游戏
                </span>              
              </div>
            </div> 
            <div>
              申博太阳城，知名顶级，极度博彩
            </div>
          </li>
          <li class="one-position">
            <div class="img">
              <div class="shade">
                <span class="enter-game">
                  进入游戏
                </span>              
              </div>
            </div> 
            <div>
              申博太阳城，知名顶级，极度博彩
            </div>
          </li>
          <li class="one-position">
            <div class="img">
              <div class="shade">
                <span class="enter-game">
                  进入游戏
                </span>              
              </div>
            </div> 
            <div>
              申博太阳城，知名顶级，极度博彩
            </div>
          </li>
          <li class="expectation">
            <div class="img">
            </div>
            <div>
              更多精彩视频直播，敬请期待
            </div>
          </li>
          <li class="expectation">
            <div class="img">
            </div>
            <div>
              更多精彩视频直播，敬请期待
            </div>
          </li>
        </ul>

      </div>
    </div>
  </section>
</template>
<script>

// import countdown from "./home/countdown";
import moreGames from "./home/moreGames";
export default {
  components: {
    // countdown,
    moreGames
  },
  name: "home",
  data() {
    return {
		//	accountVisible:false
    };
  },
  computed: {
    // aDouble: function () {
    // 	//return this.$store.state.app.getOpenTime.ExpectNo
    // },
  },
  mounted() {
    this.init();
  },
  methods: {
    init() {
      console.log("11");
    }
	}
};
</script>

<style lang="scss" >
.home{
  width: 100%;
  position:relative;
  .home-out{
    width: 100%;
    height: 5.04rem;
    background: url(../../assets/img/banner1920_504.png) no-repeat left center;
  }
  .announcement-out{
    width: 100%;
    height: 0.4rem;
    background-color: #040404;
    .announcement{
      height: 100%;
      display:flex;
      align-items: center;
      justify-content:space-between;
      // .left-marquee{
      //   display:flex;
      //   align-items: center;
      //   overflow: hidden;
      //   flex-grow: 7;
      // }
      .news{
        box-sizing: border-box;
        width: 128px;
        padding-left: 26px;
        color: #fff032;
        font-size: 12px;
        font-weight: bold;
        background: url(https://cdn.igsttech.com/Web.Portal/DQ004-01.Portal/Content/Views/Shared/images/news.png) no-repeat left center;
      }
      .marquee{
        position:relative;
        display:flex;
        width: 690px;
        overflow-x: hidden;
        white-space: nowrap;
        color:#fff;
        font-size:12px;
        ul{
          display:flex;
          align-items: center;
          cursor: pointer;
        }
      }
    }
  }
  .content-out{
    width: 100%;
    min-height: 500px;
    position: relative;
    padding: 8px 0;
    background-color: #141414;
    background-image: url(https://cdn.igsttech.com/Web.Portal/DQ004-01.Portal/Content/Views/Lobby/Live/content_bg.jpg);
    background-repeat: no-repeat;
    background-position: center top;
    .content{
      padding: 5px 0;
      background-color: #242424;
      border: 1px solid #292929;
      ul{
        display:flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
      }
      li{
        width: 320px;
        height: 307px;
        // margin: 5px;
        color: #bfbfbf;
        font-size: 12px;
        line-height: 50px;
        text-align: center;
        background-color: #383838;
        background-position: center top;
        cursor: pointer;
        margin-top: 10px;
        position: relative;
        overflow: hidden;
      }
      .two-position{
        position: relative;
        width: 650px;
        height: 307px;
        color: #fff;
        text-align: left;
        background-image: url(https://cdn.igsttech.com/Web.Portal/DQ004-01.Portal/Content/Views/Lobby/Live/ag.jpg);
        .shade{
          position: absolute;
          top: -80px;
          left: 0;
          display: inline-block;
          width: 650px;
          height: 308px;
          opacity: 0; 
          background: url(https://cdn.igsttech.com/Web.Portal/DQ004-01.Portal/Content/Views/Lobby/Live/ag_hover.png) no-repeat left top;
          transition: all ease .4s;
          &:hover{
            top:0;
            opacity: 1;
          }
        }
      }
      .one-position{       
        .shade{
          opacity: 0;
          position: absolute;
          top: -80px;
          left: 0;
          width: 320px;
          height: 257px;
          background: url(https://cdn.igsttech.com/Web.Portal/DQ004-01.Portal/Content/Views/Lobby/Live/hover_bg.png) repeat;
          transition: all ease .4s;
          .enter-game{
            display:inline-block;
            width: 120px;
            margin: 110px auto 0;
            color: #ffcf2e;
            font-size: 16px;
            line-height: 34px;
            text-align: center;
            border: 2px solid #ffcf2e;
            -moz-border-radius: 25px;
            -webkit-border-radius: 25px;
            border-radius: 25px;
          }
        }
        .img{
          &:hover{
            transform: scale(1.1);
            .shade{
              top:0;
              opacity: 1;
            }
          }
          background-image: url(https://cdn.igsttech.com/Web.Portal/DQ004-01.Portal/Content/Views/Lobby/Live/sb.jpg);
          width: 100%;
          height: 257px;
          background-repeat: no-repeat;
          background-position: center center;
          background-size: cover;
          transition: transform ease .4s;
        }
      }
      .expectation{
        .img{
          background-image: url(https://cdn.igsttech.com/Web.Portal/DQ004-01.Portal/Content/Views/Lobby/Live/more.jpg);
          width: 100%;
          height: 257px;
          background-repeat: no-repeat;
          background-position: center center;
          background-size: cover;
          transition: transform ease .4s;
        }
      }
    }
  }
}
</style>