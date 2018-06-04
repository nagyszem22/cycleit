<template>
  <div class="main-buttons">
    <div class="button fix-it" @click="$emit('setIsFixItShown')"><i class="fas fa-wrench"></i> Fix It</div>
    <div class="button recycle-it" @click="$emit('setIsRecycleItShown')"><i class="fas fa-recycle"></i> Recycle It</div>
    <div class="button materials" @click="$emit('setIsMaterialsShown')"><i class="fas fa-puzzle-piece"></i> Materials</div>
  </div>
</template>

<script>
import Icon from 'vue-awesome/components/Icon'

export default {
  name: 'MainButtons',
  components: {
    icon: Icon
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.main-buttons {
    -webkit-tap-highlight-color: transparent;
    padding: 0 50px;
    margin-top: 30px;
    text-align: center;

    .button {
      position: relative;
      width: 100%;
      height: 42px;
      line-height: 42px;
      font-size: 15px;
      color: #fff;
      margin-bottom: 12px;
      border-radius: 6px;
      background: #576574;
      border-bottom: 2px solid #222f3e;
      cursor: pointer;

      i {
        display: inline-block;
        margin-right: 6px;
      }

      &:active {
        top: 1px;
      }

      &.fix-it {
        background: #10ac84;
        border-bottom: 2px solid #0d7c5f;
      }

      &.recycle-it {
        background: #10ac84;
        border-bottom: 2px solid #0d7c5f;
      }
    }
}
</style>
