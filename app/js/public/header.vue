<template>
  <div class="header">
      <span class="left">
          <em>注册</em>&nbsp;|&nbsp;<em>登录</em>
      </span>
      <btn class="btnDownLoad" @click.native="download()">APP下载</btn>
  </div>
</template>

<script>
import btn from "../core/btn"
export default {
    components: {
        btn
    },
    methods: {
        // 跳转到APP下载界面
        download () {
            this.$router.push({name: "download"})
        }
    }
}
</script>

<style lang="scss" scoped>
.header {
    color: #666;
    height: 100px;
    line-height: 100px;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    font-size: 32px;
    background: #fff url(http://m.jr.jd.com/spe/qyy/main/images/jr-logo.png) center center no-repeat;
    background-size: auto 50%;
    z-index: 100;
    .left {
        font-size: 28px;
        height: 30px;
        line-height: 30px;
        margin: 17px 0 0 18px;
    }
    .btnDownLoad {
        float: right;
        font-size: 24px;
        border-width: 0;
        height: 56px;
        line-height: 56px;
        min-width: 120px;
        padding: 0;
        border-radius: 4px;
        margin: 28px 24px 0 0;
    }
}
</style>