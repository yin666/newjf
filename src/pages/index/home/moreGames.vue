<template>
  <section class="more-games">
    <div class="row content">
      <ul>
        <li class="one-position">
          <div class="img game_one290_215">
            <div class="shade">
              <span class="enter-game">
                进入游戏
              </span>              
            </div>
          </div>           
          <div class="description-one description">
            申博太阳城，知名顶级，极度博彩
          </div>
        </li>
        <li class="one-position">
          <div class="img game_two290_215">
            <div class="shade">
              <span class="enter-game">
                进入游戏
              </span>              
            </div>
          </div>           
          <div class="description-two description">
            申博太阳城，知名顶级，极度博彩
          </div>
        </li>
        <li class="one-position">
          <div class="img game_three290_215">
            <div class="shade">
              <span class="enter-game">
                进入游戏
              </span>              
            </div>
          </div>           
          <div class="description-three description">
            申博太阳城，知名顶级，极度博彩
          </div>
        </li>
        <li class="one-position">
          <div class="img game_four290_215">
            <div class="shade">
              <span class="enter-game">
                进入游戏
              </span>              
            </div>
          </div>           
          <div class="description-four description">
            申博太阳城，知名顶级，极度博彩
          </div>
        </li>
      </ul>
      <div class="more-click">
        <!-- <el-button type="warning" icon="el-icon-star-off" circle></el-button> -->
      </div>
    </div>
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
.more-games{
  position:relative;
  width:100%;
  position: relative;
  padding: 8px 0;
  background:#231f20;
  .content{
    padding: 5px 0;
    ul{
      display:flex;
      flex-wrap: wrap;
      justify-content: space-evenly;
    }
    li{
      width: 2.90rem;
      height: 2.15rem;
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
    .one-position{
      .description{
        position:absolute;
        width:100%;
        height: 0.42rem;
        bottom:0rem;
        left:0rem;
        line-height: 0.42rem;
        color:#fff;       
      }
      .description-one{
        background-image: linear-gradient(to right,#bae1f3 , #257de9);
      } 
      .description-two{
        background-image: linear-gradient(to right,#d8b66e , #fa513b);
      } 
      .description-three{
        background-image: linear-gradient(to right,#b454d1 , #6618af);
      }
      .description-four{
        background-image: linear-gradient(to right,#effc83 , #649a1d);
      }   
      .shade{
        opacity: 0;
        position: absolute;
        top: -80px;
        left: 0;
        width: 2.90rem;
        height: 2.15rem;
        background: url(https://cdn.igsttech.com/Web.Portal/DQ004-01.Portal/Content/Views/Lobby/Live/hover_bg.png) repeat;
        transition: all ease .4s;
        .enter-game{
          display:inline-block;
          width: 120px;
          margin: 70px auto 0 auto;
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
      .game_one290_215{
        background: url(../../../assets/img/game_one290_215.png) no-repeat left center;
      }
      .game_two290_215{
        background: url(../../../assets/img/game_two290_215.png) no-repeat left center;
      }
      .game_three290_215{
        background: url(../../../assets/img/game_three290_215.png) no-repeat left center;
      }
      .game_four290_215{
        background: url(../../../assets/img/game_four290_215.png) no-repeat left center;
      }
      .img{       
        width: 100%;
        height: 2.15rem;
        background-repeat: no-repeat;
        background-position: center center;
        background-size: cover;
        transition: transform ease .4s;
        &:hover{
          transform: scale(1.1);
          .shade{
            top:0;
            opacity: 1;
          }
        }
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
    .more-click{
      position:absolute;
      width: 0.5rem;
      height: 1rem;
    }
  }
}
</style>
