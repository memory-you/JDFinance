<template>
  <Panel
    :class="$style.more"
    title="更多福利"
  >
    <section :class="$style.content">
      <img
        src="//img12.360buyimg.com/jrpmobile/jfs/t7456/56/1425209238/21928/f1fe492d/599cee57Naea99020.jpg?width=250&height=330"
        alt
      >
      <img
        src="//img12.360buyimg.com/jrpmobile/jfs/t7894/126/1440046618/24763/5ce6a129/599cee04Ne77b3641.jpg?width=250&height=330"
        alt
      >
      <img
        src="//img12.360buyimg.com/jrpmobile/jfs/t6385/103/1675552688/24265/91be4150/59549aedNa30670f7.jpg?width=250&height=330"
        alt
      >
      <span>专享福利 ></span>
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
.more {
  @include panel;
  .content {
    @include list(row);
    justify-content: space-around;
    padding-bottom: 60px;
    position: relative;
    img {
      width: 33.333%;
      height: 280px;
      display: block;
    }
    span {
      position: absolute;
      top: -2.8rem;
      right: 0.5rem;
      height: 2.8rem;
      line-height: 2.8rem;
      font-size: 0.6rem;
      color: #999;
    }
  }
}
</style>
