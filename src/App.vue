<template>
  <div id="app">
    <Nav :navbarHeight="'50px'" />
    <Header :headerHeight="'70px'" />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Nav from "./components/Nav.vue";
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Nav,
    Header,
    Main,
    Footer,
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss">
@import "./assets/style/common.scss";
</style>
