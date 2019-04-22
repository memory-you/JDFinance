<template>
  <div>
    <Heador></Heador>
    <Rslider></Rslider>
    <Daily></Daily>
    <In></In>
    <Footor cname="mfooter"></Footor>
    <Navbar></Navbar>
  </div>
</template>

<script>
import Heador from '../public/header.vue'
import Rslider from './rslider.vue'
import Daily from './daily.vue'
import In from './in.vue'
import Footor from '../public/footer.vue'
import Navbar from '../public/navbar.vue'

export default {
  components: {
    Heador,
    Rslider,
    Daily,
    In,
    Footor,
    Navbar
  }
}
</script>

<style lang="scss" module>
@import '../../css/reset.scss';
</style>
