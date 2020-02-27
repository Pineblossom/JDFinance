<template>
  <Panel title="白条福利" :class="$style.panel">
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
            items:[{
                src: "//img12.360buyimg.com/jrpmobile/jfs/t4378/62/155957680/9017/16463551/58affd58Nb5c9198e.jpg?width=120&height=120",
                title: "开通白条",
                sub: "送188元礼包",
                em: "立即开通 >"
            },
            {
                src: "//img12.360buyimg.com/jrpmobile/jfs/t4150/330/141981421/9147/604e3e04/58affc3bNbfa8f9d7.jpg?width=120&height=120",
                title: "白条闪付",
                sub: "新手享158元礼包",
                em: "随机立减 >"
            },
            {
                src: "//img12.360buyimg.com/jrpmobile/jfs/t4270/96/1102370053/8651/58b7fa5a/58bd2e10N453e9464.jpg?width=120&height=120",
                title: "白条提额",
                sub: "金融app专享提额礼包",
                em: "去提额 >"
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
                width: 330px;
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