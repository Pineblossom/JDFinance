<template>
    <div>
        <Heador></Heador>
        <Islider></Islider>
        <Welfare></Welfare>
        <Service></Service>
        <Footer></Footer>
        <Navbar></Navbar>
    </div>
</template>

<script>
import Heador from "../public/header"
import Islider from "./islider"
import Footer from "../public/footer"
import Navbar from "../public/navbar"
import Welfare from "./welfare"
import Service from "./service"
export default {
    components: {
        Heador,
        Islider,
        Footer,
        Navbar,
        Welfare,
        Service
    }
}
</script>

<style>

</style>