<template>
  <article class="">
    <Slider
      :items="items"
      :cname="$style.slider"
    />
    <section :class="$style.list">
      <div
        :class="$style.item"
        v-for="item in enters"
        :key="item.img"
      >
        <router-link :to="{name: item.href}">
          <img
            :src="item.img"
            :alt="item.title"
          >
          <h4>{{item.title}}</h4>
        </router-link>
      </div>
    </section>
  </article>
</template>

<script>
import Slider from '../core/slider.vue'
export default {
  components: {
    Slider
  },
  data() {
    return {
      items: [
        {
          src:
            '//img12.360buyimg.com/jrpmobile/jfs/t1/23987/10/6467/33251/5c51768aE67229997/72c6ddc1b71c0b11.png?width=750&height=400',
          href: 'home'
        },
        {
          src:
            '//img12.360buyimg.com/jrpmobile/jfs/t1/17773/3/6891/54795/5c653dcdE25124e00/6d2f5d6998a597b6.jpg?width=750&height=400',
          href: 'home'
        },
        {
          src:
            '//img12.360buyimg.com/jrpmobile/jfs/t1/26590/6/7266/149007/5c6a7ab7E5a201499/3949ded503668475.png?width=750&height=400',
          href: 'home'
        },
        {
          src:
            '//img12.360buyimg.com/jrpmobile/jfs/t1/19204/26/5600/48084/5c3ed8a5Ef3ff6d5e/8dce48f9e85e7939.jpg?width=750&height=400',
          href: 'home'
        }
      ],
      enters: [
        {
          img:
            '//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132',
          href: 'download',
          title: '优惠券'
        },
        {
          img:
            '//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132',
          href: 'home',
          title: '领福利'
        },
        {
          img:
            '//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132',
          href: 'home',
          title: '抢钢镚'
        },
        {
          img:
            '//img12.360buyimg.com/jrpmobile/jfs/t1/36242/13/119/12214/5cb06492E0c73a66f/a284f91242e27af1.png?width=90&height=90',
          href: 'home',
          title: '领京豆'
        },
        {
          img:
            '//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=132&height=132',
          href: 'home',
          title: '白条提取'
        }
      ]
    }
  }
}
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.slider {
  margin-top: 120px;
  img {
    width: 100%;
  }
}
.list {
  @include list(row);
  background: #ffffff;
  padding-top: 40px;
  padding-bottom: 20px;
  justify-content: space-around;
  a {
    text-decoration: none;
  }
  .item {
    text-align: center;
    img {
      display: block;
      widows: 90px;
      height: 90px;
    }
    h4 {
      font-size: 24px;
      margin-top: 12px;
      color: #666;
    }
  }
}
</style>

