<template>
    <div>
        <Heador></Heador>
        <Slider></Slider>
        <Daily></Daily>
        <In></In>
        <More></More>
        <Footer :cname="$style.mfooter"></Footer>
        <Navbar></Navbar>
    </div>
</template>

<script>
import Heador from "../public/header"
import Footer from "../public/footer"
import Navbar from "../public/navbar"
import Slider from "./rslider.vue"
import Daily from "./daily"
import In from "./in"
import More from "./more"
export default {
    components: {
        Heador,
        In,
        Footer,
        Navbar,
        Slider,
        Daily,
        More
    }
}
</script>

<style lang="scss" module>
.mfooter {
    ul {
        >li{
            >img {
                display: none;
            }
        }
    }
}
</style>