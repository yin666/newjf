<template>
  <section class="home">
    <section class="home-out">
    </section>
    <section class="announcement-out">
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
    </section>
    <more-games></more-games>
    <section class="hot-lottery-more">
      <div class="hot-lottery-row row">
        <span class="lottery-title">
          热门彩种
        </span>
        <button class="more-g-btn">
          更多游戏
        </button>
      </div>
    </section>
    <more-lotteries></more-lotteries>
  </section>
</template>
<script>

// import countdown from "./home/countdown";
import moreGames from "./home/moreGames"
import moreLotteries from "./home/moreLotteries"
export default {
  components: {
    moreGames,
    moreLotteries
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
  .hot-lottery-more{
    width: 100%;
    height: 0.56rem;
    background-color: #231f20;
    .hot-lottery-row{
      height: 100%;
      display:flex;
      align-items: center;
      justify-content:space-between;
    }
    .lottery-title{
      color:#ddd595;
    }
    .more-g-btn{
      color: #000;
      background-image: linear-gradient(to bottom,#e8eaaf, #b5800c); 
      min-width: 0.9rem; 
      box-sizing: border-box;
      cursor: pointer;
      padding:0 0.1rem;
      height: 0.26rem;
      margin: 0 0.04rem;
      font-size: 0.13rem;
      vertical-align: top;
      border: none;
      border-radius: 0.03rem;
      transition: all .3s; 
    }
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
      .news{
        box-sizing: border-box;
        width: 128px;
        padding-left: 26px;
        color: #fff;
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
}
</style>