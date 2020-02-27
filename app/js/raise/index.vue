<template>
    <div>
        <Heador></Heador>
        <Slider></Slider>
        <Daily></Daily>
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
export default {
    components: {
        Heador,
        Footer,
        Navbar,
        Slider,
        Daily
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