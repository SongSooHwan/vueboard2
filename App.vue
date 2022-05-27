<template>
  <div id="app">
    <Header/>
    <BoardVisual/>
    <router-view/>
    <Footer/>
  </div>
</template>
<!--uptate 3 220527-->
<script>
import Header from "@/components/Header";
import BoardVisual from "@/components/BoardVisual";
import Footer from "@/components/Footer";

export default {
  name: "App",
  components: {
    Header,
    BoardVisual,
    Footer
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  color: #2c3e50;
}
.container{margin-bottom:120px;}
</style>
