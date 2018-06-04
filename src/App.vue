<template>
  <div id="app">
    <MainHeader></MainHeader>
    <VuePerfectScrollbar class="scroll-area">
      <div class="device-picture"></div>
      <div class="device-name">BaByliss 5548U Dry & Curl Diffuser Hair Dryer</div>
      <MainButtons v-on:setIsFixItShown="isFixItShown = !isFixItShown" v-on:setIsRecycleItShown="isRecycleItShown = !isRecycleItShown" v-on:setIsMaterialsShown="isMaterialsShown = !isMaterialsShown"></MainButtons>
      <transition name="custom-classes-transition" enter-active-class="animated bounceInRight" leave-active-class="animated bounceOutRight">
        <FixIt v-if="isFixItShown" v-on:setIsFixItShown="isFixItShown = !isFixItShown"></FixIt>
      </transition>
      <transition name="custom-classes-transition" enter-active-class="animated bounceInRight" leave-active-class="animated bounceOutRight">
        <RecycleIt v-if="isRecycleItShown" v-on:setIsRecycleItShown="isRecycleItShown = !isRecycleItShown"></RecycleIt>
      </transition>
      <transition name="custom-classes-transition" enter-active-class="animated bounceInRight" leave-active-class="animated bounceOutRight">
        <Materials v-if="isMaterialsShown" v-on:setIsMaterialsShown="isMaterialsShown = !isMaterialsShown"></Materials>
      </transition>
    </VuePerfectScrollbar>
  </div>
</template>

<script>
import VuePerfectScrollbar from 'vue-perfect-scrollbar';
import MainHeader from './components/MainHeader.vue';
import MainButtons from './components/MainButtons.vue';
import FixIt from './components/FixIt.vue';
import RecycleIt from './components/RecycleIt.vue';
import Materials from './components/Materials.vue';

export default {
  name: 'app',
  components: {
    MainHeader,
    MainButtons,
    FixIt,
    RecycleIt,
    Materials,
    VuePerfectScrollbar
  },
  data() {
      return {
        isFixItShown: false,
        isRecycleItShown: false,
        isMaterialsShown: false
      }
  }
}
</script>

<style lang="less">
#app {
  position: fixed;
  right: 0;
  top: 0;
  left: 0;
  bottom: 0;
  font-family: 'Roboto', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;

  .scroll-area {
    position: absolute;
    right: 0;
    top: 60px;
    left: 0;
    bottom: 0;
    background: #f2f2f2;

    .device-picture {
      position: absolute;
      width: 120px;
      height: 120px;
      left: 50%;
      margin-left: -60px;
      border-radius: 66px;
      margin-top: 20px;
      border: 6px solid #10ac84;
      background-image: url('./assets/hairdryer.jpeg');
      background-repeat: no-repeat;
      background-position: center center;
      -webkit-background-size: contain;
      -moz-background-size: contain;
      -o-background-size: contain;
      background-size: contain;
    }

    .device-name {
      margin-top: 165px;
      text-align: center;
      color: #222;
      font-size: 18px;
      padding: 0 30px;
      font-weight: 300;
      line-height: 26px
    }      
  }
}
</style>
