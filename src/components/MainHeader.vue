<template>
  <div class="main-header">
    CycleIt.
  </div>
</template>

<script>
export default {
  name: 'MainHeader'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.main-header {
    position: absolute;
    right: 0;
    top: 0;
    left: 0;
    z-index: 1000;
    height: 60px;
    line-height: 60px;
    padding-left: 15px;
    font-size: 18px;
    font-family: 'Merriweather', serif;
    font-weight: 600;
    background: #10ac84;
    color: #fff;
    box-shadow: 0 3px 10px rgba(0,0,0,0.16), 0 3px 10px rgba(0,0,0,0.23);
  }
</style>
