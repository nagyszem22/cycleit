<template>
  <div class="page-container"> 
    <div class="page-header">
      <div class="back-button" @click="$emit('setIsMaterialsShown')">
        <i class="fas fa-arrow-left"></i>
      </div>
      <div class="title">Materials.</div>
    </div>
    <VuePerfectScrollbar :class="'content-box'">
      
    </VuePerfectScrollbar>
  </div>
</template>

<script>
import Icon from 'vue-awesome/components/Icon';
import VuePerfectScrollbar from 'vue-perfect-scrollbar';

export default {
  name: 'Materials',
  components: {
    VuePerfectScrollbar
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.page-container {
  position: fixed;
  right: -50px;
  top: 0;
  left: 0;
  padding-right: 50px; 
  bottom: 0;
  z-index: 2000;
  background: #fff;
  box-shadow: 0 -20px 22px rgba(0, 0, 0, .4);
  border-top: 1px solid #ccc;

  .page-header {
    position: absolute;
    right: 0;
    top: 0;
    left: 0;
    padding-right: 50px; 
    z-index: 1000;
    height: 58px;
    line-height: 58px;
    text-align: center;
    box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);

    .back-button {
      position: absolute;
      top: 0;
      left: 0;
      width: 60px;
      height: 58px;
      font-size: 20px;
      color: #666;

      &:hover {
        color: #222;
      }

      &:active {
        top: 1px;
      }
    }
  }

  .content-box {
    overflow: hidden;
    position: absolute;
    right: 0;
    top: 58px;
    left: 0;
    bottom: 58px;
    padding: 20px 70px 10px 20px;
    font-size: 14px;
  }
}
</style>
