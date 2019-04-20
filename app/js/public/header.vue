<template>
    <!-- 在style标签标明 module后  可以使用$style去绑定类名  -->
    <div :class="$style.header">
        <span :class="$style.left">
            <em>注册</em>&nbsp;|&nbsp;
            <em>登录</em>
        </span>
        <btn :class="$style.btnDownload">APP下载</btn>
    </div>
</template>

<script>
import btn from "../core/btn.vue";
export default {
    components: {
        btn
    }
};
</script>

<style  lang="scss" module>
.header {
    height: 100px;
    line-height: 100px;
    color: #666;
    font-size: 32px;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    background: #fff url("//m.jr.jd.com/spe/qyy/main/images/jr-logo.png")
        no-repeat center center;
    background-size: auto 50%;
    z-index: 100;
    .left {
        font-size: 28px;
        height: 30px;
        line-height: 30px;
        margin: 17px 0 0 18px;
    }
    .btnDownload {
        font-size: 24px;
        height: 56px;
        line-height: 56px;
        min-width: 120px;
        border-radius: 4px;
        padding: 0;
        border-width: 0;
        margin: 28px 24px 0 0;
        float: right;
    }
}
</style>