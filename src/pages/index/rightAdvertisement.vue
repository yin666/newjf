<template>
  <aside class="right-advertise">   
  </aside>
</template>

<script>
  export default {
    name: 'right-advertise',
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
.right-advertise{
  position: fixed;
  width: 120px;
  height: 352px;
  top:30%;
  right: 0;
  background-position: left top;
}
</style>
