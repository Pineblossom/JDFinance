<template>
  <Panel title="新品推荐" :class="$style.panel">
      <section :class="$style.concent">
          <div>更多尖货></div>
          <Slider :options="options" :items="items" cname="product-slider"></Slider>
      </section>
  </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import Slider from "../core/slider.vue"
export default {
    components: {
        Panel,
        Slider
    },
    data () {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/90292/3/12848/137217/5e4fcdd5Ed633e2af/8edbe784390886ea.jpg!q70"
            },
            {
                href: "home",
                src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/96268/12/1735/50303/5dc4c314Ec2837a84/16ff6cf3b4143fcd.jpg!q70"
            },
            {
                href: "home",
                src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/94930/16/1528/149807/5dc0ed5cE8868ed35/eb55b9c8f5142194.jpg!q70"
            },
            {
                href: "home",
                src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/90494/4/11721/139090/5e3a63e3Ea01e1fa8/79679eaf0e6770e6.jpg!q70"
            },
            {
                href: "home",
                src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/110384/30/95/149782/5df2664aEbcfd8b7c/016f49a248c5f03d.jpg!q70"
            }],
            options:{
                // pagination: {
                //     el: ".swiper-pagination",
                //     clickable: true
                // },
                slidesPerView: 2.3,
                spaceBetween: 30,
                freeMode: true
            }
        }
    }
}
</script>

<style lang="scss">
.prodect-slider {
    .swiper-container {
        box-sizing: border-box;
        padding: 0 24px;
        .swiper-slider {
            .a {
                display: inline-block;
                width: 100%;
                img {
                    width: 100%;
                    display: block;
                    height: 314px;
                    border: 1px solid #fafafa;
                }
            }
        }
    }
}
</style>
<style lang="scss" module>
@import "../../css/element.scss";
.panel {
    @include panel;
    .concent {
        padding: 40px;
        position: relative;
        &>div {
            position: absolute;
            font-size: 28px;
            color: #999;
            right: 20px;
            top: -75px
        }
    }
}
</style>