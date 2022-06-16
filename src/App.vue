<template>
  <TmpHeader />
  <TmpMain />
  <TmpFooter />
</template>

<script>
import TmpFooter from "./components/template/TmpFooter.vue";
import TmpHeader from "./components/template/TmpHeader.vue";
import TmpMain from "./components/template/TmpMain.vue";
export default {
  name: "App",
  components: { TmpHeader, TmpMain, TmpFooter },
};
</script>

<style lang="scss">
@import "./assets/style/style.scss";
.svg-inline--fa {
  vertical-align: -3px;
}
</style>
