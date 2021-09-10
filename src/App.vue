<template>
  <div id="app">
    <Header @findValue="searchValue" />
    <Main :selectValue="selectValue" />
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
  data() {
    return {
      selectValue: "",
    };
  },
  methods: {
    searchValue(value) {
      this.selectValue = value;
    },
  },
};
</script>

<style lang="scss">
@import "scss/style.scss";
body {
  background-color: rgb(1, 46, 129);
}
</style>
