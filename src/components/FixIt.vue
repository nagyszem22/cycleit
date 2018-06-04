<template>
  <div class="page-container"> 
    <div class="page-header">
      <div class="back-button" @click="$emit('setIsFixItShown')">
        <i class="fas fa-arrow-left"></i>
      </div>
      <div class="title">Fix It.</div>
    </div>
    <VuePerfectScrollbar :class="'content-box'">
      <iframe width="100%" height="200px" src="https://www.youtube.com/embed/RFgATtKjl2k" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
      <div class="steps">

        <div class="header">
          <div class="label">1</div>
          <div class="title">Shell</div>
        </div>
        <div class="content">Unscrew the two 17.83 mm black screws located on the handle.</div>

        <div class="header">
          <div class="label">2</div>
          <div class="title">Separation</div>
        </div>
        <div class="content">Separate the shell from the main component.<br>Make sure that the each piece is free from debris.</div>

        <div class="header">
          <div class="label">3</div>
          <div class="title">Pull components apart</div>
        </div>
        <div class="content">Continue to pull the components apart.<br>For reassembly, put the silver encasing on before the the black cover.</div>

        <div class="header">
          <div class="label">4</div>
          <div class="title">Disassembly</div>
        </div>
        <div class="content">Take the head of the hairdryer and pull the pieces apart.</div>

        <div class="header">
          <div class="label">5</div>
          <div class="title">Remove the vent</div>
        </div>
        <div class="content">Remove the black vent from the grey cylindrical piece.</div>

        <div class="header">
          <div class="label">6</div>
          <div class="title">Extract lint</div>
        </div>
        <div class="content">If there is lint in the vent, use tweezers or a toothbrush to extract it from the vent.<br>This will keep the fan from getting clogged and malfunctioning.</div>

        <div class="header">
          <div class="label">7</div>
          <div class="title">Clean components</div>
        </div>
        <div class="content">Clean the other black vent with a toothbrush.</div>

        <div class="header">
          <div class="label">8</div>
          <div class="title">Clean the rest</div>
        </div>
        <div class="content">Clean these two components with a paper towel.</div>
      </div>
    </VuePerfectScrollbar>
  </div>
</template>

<script>
import Icon from 'vue-awesome/components/Icon';
import VuePerfectScrollbar from 'vue-perfect-scrollbar';

export default {
  name: 'FixIt',
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
    bottom: 0;
    padding: 0 50px 0 0;
    font-size: 14px;
  }
}
</style>
