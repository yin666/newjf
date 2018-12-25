<template>
  <section class="more-lotteries">
    <div class="row content">
      <div class="left" @click="shiftLeft">
        <
      </div>
      <div class="right" @click="shiftRight">
        >
      </div>
      <ul class="lottery-ul" :style="{width: ulWidth}">
        <li v-for="(item, index) in lotteries" :key="item.name" :index="index">
          <img :src=item.img alt="">
          <div class="lottery-li-name">{{item.name}}</div>
        </li>
      </ul>
    </div>
  </section>   
</template>

<script>
import img from "../../../assets/img/lottery (3).png"
  export default {
    name: 'more-lotteries',
    props: [],
    data() {
      return {
        ulWidth:"12.61rem",
        lotteries:[
          {img:"static/img/lottery (1).png",name:"幸运28",num:0},
          {img:"static/img/lottery (2).png",name:"重庆时时彩",num:1},
          {img:"static/img/lottery (3).png",name:"北京PK10",num:2},
          {img:"static/img/lottery (4).png",name:"山东11选5",num:3},
          {img:"static/img/lottery (5).png",name:"广东11选5",num:4},
          {img:"static/img/lottery (6).png",name:"北京快乐8",num:5},
          {img:"static/img/lottery (7).png",name:"湖北快三",num:6},
          {img:"static/img/lottery (8).png",name:"重庆快乐10分",num:7},
          {img:"static/img/lottery (9).png",name:"福彩3D",num:8},
          {img:"static/img/lottery (1).png",name:"幸运282",num:9},
          {img:"static/img/lottery (3).png",name:"北京PK102",num:10}
        ],
        msg: 'more-lotteries'
      }
    },
    methods: {
      init() { 
        this.setUlWidth();     
      },
      shiftLeft(){//  点击向左滑动箭头
        if(this.lotteries.length - this.lotteries[0].num < 10){//滑到最后一个了，不可以滑了
        }else{ //可以滑动
          let tmp = this.lotteries.shift();
          this.lotteries.push(tmp);
        }     
      },
      shiftRight(){// 点击向右滑动箭头
        if(this.lotteries[0].num === 0){  //在初始位置，不可以滑动
        }else{  //可以滑动
          let tmp = this.lotteries.pop();
          this.lotteries.unshift(tmp);
        }      
      },
      setUlWidth() {//  设置ul的宽度
        this.ulWidth = this.lotteries.length * 1.32 +'rem';
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
.more-lotteries{
  position:relative;
  width:100%;
  padding: 8px 0;
  background:#231f20;
  border-bottom:1px solid #393536;
  .content{
    padding: 5px 0;
    height: 1.5rem;
    overflow-x: hidden;
  }
  .lottery-ul{
    position:relative;
    width:11.61rem;
    display:flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    margin-left: auto;
    margin-right: auto;
    flex-wrap: nowrap;
    padding-left: 0.05rem;
    padding-right: 0.05rem;
    li{
      cursor: pointer;
      flex-basis:1.29rem;
    }
    img{
      width: 1.02rem;
    }
  }
  .lottery-li-name{
    margin-top:0.05rem;
    text-align: center;
    color:#fff;
  }
  %position-shared {
    position:absolute;
    width: 0.18rem;
    height: 0.18rem;
    border-radius: 50%;
    background:#9a9899;
    top:0.5rem;
    text-align: center;
    line-height: 0.18rem;
    color:#000;
    cursor: pointer;
    z-index: 20;
  }
  .left{
    @extend %position-shared;
    left:0rem;
    
  }
  .right{
    @extend %position-shared;
    right:0rem;
  }
}
</style>
