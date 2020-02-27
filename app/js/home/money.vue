<template>
  <Panel title="理财精选">
      <section :class="$style.concent">
          <dl :class="$style.item" v-for="(item, index) in items" :key="index">
              <dt>{{ item.title }}<span>{{ item.sub }}</span></dt>
              <dd>{{ item.rate }}</dd>
              <dd>{{ item.text }}</dd>
          </dl>
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
                title: "定期理财",
                sub: "理财首选",
                rate: "5.60%",
                text: "历史年化回报率"
            },
            {
                title: "小白理财",
                sub: "理财首选",
                rate: "4.22%",
                text: "七日年化收益率"
            },
            {
                title: "月月盈",
                sub: "养老保障",
                rate: "5%",
                text: "七日年化收益率"
            },
            {
                title: "小白基金",
                sub: "天天赚钱",
                rate: "4.27%",
                text: "七日年化收益率"
            }]
        }
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
}
.concent {
    @include flex(row);
    justify-content: space-around; // 在弹性盒对象的 <div> 元素中的各项周围留有空白
    box-sizing: border-box;
    &:after {
        content: " ";
        display: block;
        width: 100%;
        height: 0px;
        position: relative;
        top: -208px;
        border-bottom: 1px solid #ddd;
        box-sizing: border-box;
    }
    .item {
        position: relative;
        width: 50%;
        box-sizing: border-box;
        padding: 34px 16px;
        &:after {
            content: " ";
            width: 1px;
            height: 136px;
            display: block;
            position: absolute;
            top: 50%;
            right: 0;
            margin-top: -68px;
            border-right: 1px solid #999;
        }
        &:nth-child(2n) {
            &:after {
                display: none;
            }
        }
        dt {
            font-size: 30px;
            line-height: 42px;
            color: #333;
            span {
                font-size: 22px;
                color: #ff5155;
                border: 1px solid #ff5155;
                padding: 0 8px;
                vertical-align: 1px; // 设置元素的垂直对齐方式
                margin-left: 2px;
            }
        }
        dd {
            &:nth-child(2) {
                font-weight: 700;
                font-size: 44px;
                height: 58px;
                line-height: 58px;
                color: #ff5155;
                white-space: nowrap; // 规定段落中的文本不进行换行
                text-overflow: ellipsis; // 显示省略符号来代表被修剪的文本。
                overflow: hidden; // 内容会被修剪，并且其余内容是不可见的。
            }
            &:nth-child(3) {
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
</style>