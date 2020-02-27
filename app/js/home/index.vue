<template lang="html">
    <div>
        <Heador></Heador>
        <Hslider></Hslider>
        <Novice></Novice>
        <Borrow></Borrow>
        <Money></Money>
        <Prodect></Prodect>
        <Life></Life>
        <Footer></Footer>
        <Navbar></Navbar>
    </div>
</template>

<script>
import Heador from "../public/header"
import Hslider from "../home/hslider"
import Novice from "../home/novice"
import Borrow from "../home/borrow"
import Money from "../home/money"
import Prodect from "../home/product"
import Life from "../home/life"
import Footer from "../public/footer"
import Navbar from "../public/navbar"
export default {
    components: {
        Heador,
        Hslider,
        Novice,
        Borrow,
        Money,
        Prodect,
        Life,
        Footer,
        Navbar
    }
}
</script>

<style lang="scss" module>
</style>
