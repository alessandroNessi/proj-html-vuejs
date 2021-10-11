<template>
  <div id="app">
    <Nav/>
    <Header/>
    <Main/>
    <Footer/>
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
};
</script>

<style lang="scss">

</style>
