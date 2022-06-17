<template>
  <footer>
    <TmpFooterTop />
    <TmpFooterBot />
  </footer>
</template>

<script>
import TmpFooterBot from "./footer/TmpFooterBot.vue";
import TmpFooterTop from "./footer/TmpFooterTop.vue";
export default {
  components: { TmpFooterBot, TmpFooterTop },
  name: "TmpFooter",
};
</script>

<style lang="scss" scoped>
</style>