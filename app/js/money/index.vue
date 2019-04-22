<template>
  <div>
    <Heador></Heador>
    <Slider></Slider>
    <Ada></Ada>
    <Money></Money>
    <Adb></Adb>
    <Finance></Finance>
    <Adc></Adc>
    <Footor></Footor>
    <Navbar></Navbar>
  </div>
</template>

<script>
import Heador from '../public/header.vue'
import Slider from './mslider.vue'
import Ada from './ada.vue'
import Money from './money.vue'
import Adb from './adb.vue'
import Finance from './finance.vue'
import Adc from './adb.vue'
import Footor from '../public/footer.vue'
import Navbar from '../public/navbar.vue'

export default {
  components: {
    Heador,
    Slider,
    Ada,
    Money,
    Adb,
    Finance,
    Adc,
    Footor,
    Navbar
  }
}
</script>

<style lang="scss" module>
@import '../../css/reset.scss';
.home {
  color: red;
  font-size: 80px;
}
</style>
