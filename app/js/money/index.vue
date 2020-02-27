<template>
    <div>
        <Heador></Heador>
        <Navbar></Navbar>
        <Mslider></Mslider>
        <Money></Money>
        <Adv></Adv>
        <Finance></Finance>
        <Invest></Invest>
        <Footer :cname="$style.mfooter"></Footer>
    </div>
</template>

<script>
import Heador from "../public/header"
import Navbar from "../public/navbar"
import Mslider from "./mslider"
import Money from "./money"
import Adv from "./adv"
import Finance from "./finance"
import Footer from "../public/footer"
import Invest from "./invest"
export default {
    components: {
        Heador,
        Navbar,
        Mslider,
        Money,
        Adv,
        Finance,
        Footer,
        Invest
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