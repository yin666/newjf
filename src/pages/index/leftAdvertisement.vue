<template>
  <aside class="left-advertise">
    
  </aside>
</template>

<script>
  export default {
    name: 'left-advertise',
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
.left-advertise{
  position: fixed;
  width: 120px;
  height: 352px;
  top:30%;
  left: 0;
  background-position: right top;
}
</style>
