<template>
  <Panel title="理财精选" :cname="$style.panel">
      <ul :class="$style.content" v-for="(item, index) in items" :key="index">
          <li :class="$style.item">
              <img :src="item.src" alt="">
              <div>
                  <h4>{{ item.title }}</h4>
                  <p>{{ item.sub }}</p>
              </div>
              <em>{{ item.em }}</em>
          </li>
      </ul>
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
                src: "//img12.360buyimg.com/jrpmobile/jfs/t3670/58/543125556/2606/a65096b9/580d80afN63b1085a.png?width=76&height=76",
                title: "月度理财",
                sub: "预期年化收益率4.50%",
                em: "去赚钱 >"
            },
            {
                src: "//img12.360buyimg.com/jrpmobile/jfs/t3679/44/511862277/2728/c1c6b2bf/580d8189N6b6f8052.png?width=76&height=76",
                title: "季度理财",
                sub: "历史年化回报率5.50%",
                em: "去赚钱 >"
            },
            {
                src: "//img12.360buyimg.com/jrpmobile/jfs/t3331/69/580199498/3074/d5bb21c5/580d7f6cN7f35e596.png?width=76&height=76",
                title: "一年理财",
                sub: "历史年化回报率5.80%",
                em: "去赚钱 >"
            }]
        }
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    >h4 {
        border-bottom: 1px solid #ddd;
    }
    .content {
        @include list;
        box-sizing: border-box;
        &:last-child::after {
            border-color: #fff;
        }
        .item {
            height: 140px;
            line-height: 140px;
            align-items: center;
            @include list(row);
            &::after {
                content: " ";
                width: 100%;
                height: 0;
                border-top: 1px solid #ddd;
                box-sizing: border-box;
                margin-left: 133px;
            }
            img {
                height: 88px;
                width: 88px;
                display: inline-block;
                margin: 0 32px;
            }
            >div {
                width: 344px;
                color: #333;
                line-height: 1.8;
                >h4 {
                    font-size: 32px;
                }
                >p {
                    font-size: 24px;
                    color: #ff5151;
                    white-space: nowrap;
                    text-overflow: ellipsis;
                    overflow: hidden;
                }
            }
            >em {
                color: #FF801A;
                font-size: 28px;
            }
        }
    }
}
</style>