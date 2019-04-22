<template>
  <Panel
    :class="$style.rslider"
    title="金融头条"
  >
    <section :class="$style.content">
      <swiper :options="swiperOption">
        <swiper-slide>
          百万白条券免费送，速来领取！！
          <em>></em>
        </swiper-slide>
        <swiper-slide>
          签到领流量，1元500M！
          <em>></em>
        </swiper-slide>
      </swiper>
    </section>
  </Panel>
</template>

<script>
import Panel from '../core/panel.vue'
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
  components: {
    Panel,
    swiper,
    swiperSlide
  },
  data() {
    return {
      swiperOption: {
        autoplay: true,
        loop: true,
        direction: 'vertical'
      }
    }
  }
}
</script>

<style module lang="scss">
@import '../../css/element.scss';
.rslider {
  @include panel;
  margin-top: 120px !important;
  > h4 {
    display: none;
  }
  .content {
    height: 72px;
    line-height: 72px;
    padding-left: 178px;
    background: url(//m.jr.jd.com/spe/qyy/main/images/scroll_title_img.png) left
      center no-repeat;
  }
}
</style>
<style lang='scss' scoped>
.swiper-container {
  height: 72px;
  overflow: hidden;
  .swiper-slide {
    height: 72px;
    color: #333;
    font-size: 28px;
    font-family: 'PingFang-media';
    overflow: hidden;
    text-overflow: ellipse;
    white-space: nowrap;
    em {
      color: #ddd;
      float: right;
      margin-right: 30px;
    }
  }
}
</style>
