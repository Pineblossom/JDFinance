<template>
  <Panel :class="$style.panel" title="生活服务">
      <section :class="$style.concent">
          <ul :class="$style.item" v-for="(item, index) in items" :key="index">
              <li>
                  <img :src="item.src" alt="">
                  <p>{{ item.main }}</p>
                  <p>{{ item.sub }}</p>
              </li>
          </ul>
      </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel"
export default {
    components: {
        Panel
    },
    data () {
        return {
            items: [{
                src: "//img12.360buyimg.com/jrpmobile/jfs/t4375/104/1184122472/3976/89741da4/58be8a6eNf10193d0.png?width=135&height=135",
                main: "惠加油",
                sub: ""
            },
            {
                src: "//img12.360buyimg.com/jrpmobile/jfs/t4747/185/1901740991/5892/1383fb93/58f57851N17ee6993.jpg?width=132&height=132",
                main: "小白信用",
                sub: "全新升级"
            },
            {
                src: "//img12.360buyimg.com/jrpmobile/jfs/t3241/234/8044685271/3713/7b29f77f/58be89c8Nb9d41295.png?width=135&height=135",
                main: "信用卡还款",
                sub: ""
            },
            {
                src: "//img12.360buyimg.com/jrpmobile/jfs/t3172/259/7993557249/4351/fd082707/58be8a81Nd7716a06.png?width=135&height=135",
                main: "卡转让",
                sub: ""
            },
            {
                src: "//img12.360buyimg.com/jrpmobile/jfs/t3085/320/8107659086/4344/cdbba2dd/58be8acfNdadcaf00.png?width=135&height=135",
                main: "定期还款",
                sub: ""
            },
            {
                src: "",
                main: "",
                sub: ""
            }]
        }
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    .concent {
        @include list(row);
        box-sizing: border-box;
        .item {
            width: 20%;
            text-align: center;
            img {
                width: 90px;
                height: 90px;
                line-height: 90px;
            }
            p {
                font-size: 26px;
                color: #666;
                white-space: nowrap;
                text-overflow: ellipsis;
                overflow: hidden;
                margin-top: 12px;
            }
            p:nth-child(3) {
                color: #ff5151;
            }
        }
    }
}
</style>