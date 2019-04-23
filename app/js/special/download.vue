<template>
  <Panel
    :class="$style.special"
    title="APP下载"
  >
    <section :class="$style.content">
      <div></div>
      <p>立即下载</p>
      <span>copyright</span>
    </section>
  </Panel>
</template>

<script>
import Panel from '../core/panel.vue'
export default {
  components: {
    Panel
  }
}
</script>

<style module lang="scss">
@import '../../css/element.scss';
html,
body {
  background: #fff;
}
.special {
  > h4 {
    display: none;
  }
  @include panel;
  margin: 0 !important;
  .content {
    @include list(column);
    align-items: center;
    justify-content: center;
    height: 1136px;
    > div {
      background: url(https://img12.360buyimg.com/jrpmobile/jfs/t8956/285/1249806938/50853/8cd3c8f0/59b65f36N05367075.png?)
        center center no-repeat;
      width: 600px;
      height: 800px;
      background-size: 100% auto;
      margin-top: -230px;
    }
    > p {
      @include btn($size: 32px, $color: #fff, $bgcolor: #f1443e, $padding: 0px);
      height: 100px;
      width: 470px;
      line-height: 100px;
      border-radius: 5px;
      box-shadow: 0 12px 32px 0 rgba(255, 159, 135, 0.6);
      position: fixed;
      bottom: 130px;
    }
    span {
      position: fixed;
      bottom: 16px;
      color: #ddd;
      font-size: 24px;
    }
  }
}
</style>
