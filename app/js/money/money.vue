<template>
  <Panel
    title="理财精选"
    :class="$style.money"
  >
    <section :class="$style.content">
      <div
        :class="$style.item"
        v-for="item in items"
        :key="item.title"
      >
        <dl>
          <dt>
            {{item.title}}
            <span>{{item.subtitle}}</span>
          </dt>
          <dd>{{item.rate}}</dd>
          <dd>{{item.text}}</dd>
        </dl>
      </div>
    </section>
  </Panel>
</template>

<script>
import Panel from '../core/panel.vue'
export default {
  components: {
    Panel
  },
  data() {
    return {
      items: [
        {
          title: '定期理财',
          subtitle: '理财首选',
          rate: '5.66%',
          text: '管理你的财富'
        },
        {
          title: '小白理财',
          subtitle: '理财首选',
          rate: '4.26%',
          text: '七日年化收益率'
        },
        {
          title: '月月盈',
          subtitle: '养老保障',
          rate: '5.00%',
          text: '七日年化收益率'
        },
        {
          title: '小白基金',
          subtitle: '天天赚钱',
          rate: '4.17%',
          text: '七日年化收益率'
        }
      ]
    }
  }
}
</script>

<style module lang="scss">
@import '../../css/element.scss';
.money {
  @include panel;
  .content {
    @include list(row);
    position: relative;
    &::before {
      content: '';
      display: block;
      width: 100%;
      height: 50%;
      border-bottom: 1px solid #eee;
      box-sizing: border-box;
      position: absolute;
      top: 0;
    }
    .item {
      box-sizing: border-box;
      width: 50%;
      position: relative;
      padding: 34px 16px;
      &::after {
        content: '';
        display: block;
        width: 1px;
        height: 136px;
        position: absolute;
        top: 50%;
        right: 0;
        margin-top: -68px;
        border-right: 1px solid #eee;
      }
      &:nth-child(2n) {
        &::after {
          display: none;
        }
      }
      dt {
        font-size: 30px;
        line-height: 42px;
        color: #333;
        span {
          font-size: 24px;
          color: #ff5155;
          border: 1px solid #ff5155;
          padding: 0 8px;
          margin-left: 2px;
          vertical-align: 1px;
        }
      }
      dd {
        &:nth-of-type(1) {
          font-weight: 700;
          font-size: 44px;
          height: 58px;
          line-height: 58px;
          color: #ff5155;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
        }
        &:nth-of-type(2) {
          font-size: 24px;
          height: 34px;
          line-height: 34px;
          color: #999;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
        }
      }
    }
  }
}
</style>