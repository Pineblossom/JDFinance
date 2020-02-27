<template lang="html">
      <article class="">
            <Slider :items="items" :cname="$style.slider"></Slider>
            <section :class="$style.list">
                <div :class="$style.item" v-for="item in enters" :key="item.img">
                    <router-link :to="{ name: item.href }">
                        <img :src="item.img" :alt="item.title"/>
                        <h4>{{ item.title }}</h4>
                    </router-link>
                </div>
            </section>
      </article>
</template>

<script>
import Slider from "../core/slider.vue"
export default {
    components: {
        Slider
    },
    data () {
        return {
            items: [{   // 轮播图
                href: "home",
                src: "//img20.360buyimg.com/mcpageview/jfs/t1/95208/39/9858/41488/5e11d67eE007e4d4b/c7fe2048ac932c6f.jpg"
            },
            {
                href: "home",
                src: "//img20.360buyimg.com/mcpageview/jfs/t1/106678/1/12210/92914/5e4535daE1770d4c3/30137746303353c1.jpg"
            },
            {
                href: "home",
                src: "//img20.360buyimg.com/mcpageview/jfs/t1/93607/27/9768/38387/5e11d688E04270824/2d9495f7de2365ca.jpg"
            },{
                href: "home",
                src: "//img20.360buyimg.com/mcpageview/jfs/t1/110275/24/5594/177559/5e3d5994Ed4157b19/5aba23174ace9305.jpg"
            }],
            enters: [{  // 列表
                href: "home",
                img: "//img20.360buyimg.com/mcpageview/jfs/t1/101844/12/9760/11216/5e11d703Ec915a9b9/014b4c8a90f4f970.png",
                title: "优惠券"
            },
            {
                href: "home",
                img: "//img20.360buyimg.com/mcpageview/jfs/t1/85137/14/9816/10770/5e11d7ddE2805969c/9f4f3cdcfeb204e5.png",
                title: "领红包"
            },
            {
                href: "home",
                img: "//img20.360buyimg.com/mcpageview/jfs/t1/90523/1/9767/16031/5e11d735E29291893/7ea1474e22f075a3.png",
                title: "抢钢镚"
            },
            {
                href: "home",
                img: "//img20.360buyimg.com/mcpageview/jfs/t1/105209/4/9857/12579/5e11d770E4e458bc7/fbbbec1918b041e3.png",
                title: "领京豆"
            },
            {
                href: "home",
                img: "//img20.360buyimg.com/mcpageview/jfs/t1/94998/29/9746/11665/5e11d753E53811340/b555a3fb637dad6d.png",
                title: "白条提额"
            }]
        }
    }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.slider {
    margin-top: 120px;
    img {
        width: 100%;
        height: 100%;
    }
}
.list {
    @include list(row);
    background: #fff;
    padding-top: 40px;
    padding-bottom: 20px;
    justify-content: space-around; // 两端对齐
    a {
        text-decoration: none; // 没有下划线
    }
    .item {
        text-align: center;
        img {
            display: inline-block;
            width: 90px;
            height: 90px;
        }
        h4 {
            font-size: 26px;
            margin-top: 12px;
            color: #666;
        }
    }
}
</style>