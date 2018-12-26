<template>
  <div class="template">
    <h2 class="red">about vuex</h2>
    <div>get vuex</div>
    <div><span>this.$store.state.user.AcctAmount :</span> <span>{{getVuex}}</span></div>
    <div>set vuex</div>
    <div><span>this.$store.commit('setAccesstoken', "11");</span></div>
    <router-view/>
    <right-advertisement></right-advertisement>
  </div>
</template>

<script>
import rightAdvertisement from "./index/rightAdvertisement"
export default {
  name: 'HelloWorld',
  components: {    
    rightAdvertisement
  },
  data () {
    return {
      getVuex: this.$store.state.user.AcctAmount
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang='scss'>
.template{
  color:#fff;
  .red{
    color:red;
  }
}
</style>
