<template>
  <section class="real-person">
    <div class="banner">
    </div>
    <div class="photos row">
      <ul class="photos-ul">
        <li @mouseenter="hoverLi" @mouseleave="leaveLi" ></li>
        <li @mouseenter="hoverLi" @mouseleave="leaveLi" ></li>
        <li @mouseenter="hoverLi" @mouseleave="leaveLi" ></li>
        <li @mouseenter="hoverLi" @mouseleave="leaveLi" ></li>
        <li @mouseenter="hoverLi" @mouseleave="leaveLi" ></li>
        <li @mouseenter="hoverLi" @mouseleave="leaveLi" ></li>
        <li @mouseenter="hoverLi" @mouseleave="leaveLi" ></li>
        <li @mouseenter="hoverLi" @mouseleave="leaveLi" ></li>
      </ul>

    </div>

  </section>
</template>
<script>

// import countdown from "./home/countdown";
export default {
  components: {
    //advantageContent
  },
  name: "real-person",
  data() {
    return {
      ifHover:false //如果是fasle为没有悬浮，如果是true表示悬浮
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
    hoverLi(e){
      e.currentTarget.classList.add("hover")
    },
    leaveLi(e){
      e.currentTarget.classList.remove("hover")
    },
    init() {
      console.log("11");
    }
	}
};
</script>

<style lang="scss" >
.real-person{
  position:relative;
  width: 100%;
  margin: 0 auto;
  background-color:#440c00;
  .banner{
    width: 19.20rem;
    height: 3rem;
    background: url(../../assets/img/copy-banner.jpg) no-repeat left center;
  }
  .photos{
    display: flex;
  }
  .photos-ul{
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    justify-content: center;
    >li{
      width: 2.42rem;
      height: 3.08rem;
      background: url(../../assets/img/copy-ad.jpg) no-repeat;
      margin:0.1rem 0.05rem 0.1rem 0.05rem;
      cursor: pointer;
    }
    .hover{
      background-position: left bottom;
    } 
    .leave{
      background-position: left top;
    }  
  }
}
</style>