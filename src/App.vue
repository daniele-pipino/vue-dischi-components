<template>
  <div id="app">
    <Header />
    <Main />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Main from "@/components/Main.vue";
export default {
  name: "App",
  components: {
    Header,
    Main,
  },
};
</script>

<style lang="scss">
@import "scss/style.scss";
body {
  background-color: rgb(1, 46, 129);
}
</style>
