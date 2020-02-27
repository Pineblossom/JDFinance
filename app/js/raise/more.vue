<template>
  <Panel title="更多福利" :class="$style.panel">
      <section :class="$style.content">
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t7456/56/1425209238/21928/f1fe492d/599cee57Naea99020.jpg?width=250&height=330" alt="">
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t7894/126/1440046618/24763/5ce6a129/599cee04Ne77b3641.jpg?width=250&height=330" alt="">
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t6385/103/1675552688/24265/91be4150/59549aedNa30670f7.jpg?width=250&height=330" alt="">
        <P>专享福利 > </P>
      </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel"
export default {
    components: {
        Panel
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    .content {
        @include list(row);
        position: relative;
        margin-bottom: 40px;
        img {
            width: 33.333333%;
            height: 240px;
        }
        p {
            position: absolute;
            font-size: 24px;
            color: #666;
            right: 20px;
            top: -68px;
        }
    }
}
</style>