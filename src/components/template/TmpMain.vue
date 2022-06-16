<template>
  <main>
    <TmpHero />
    <TmpDream />
    <TmpCarrier />
    <TmpInfo />
    <TmpCourse />
    <TmpLearn />
    <TmpMobile />
  </main>
</template>

<script>
import TmpHero from "./section/TmpHero.vue";
import TmpDream from "./section/TmpDream.vue";
import TmpCarrier from "./section/TmpCarrier.vue";
import TmpInfo from "./section/TmpInfo.vue";
import TmpCourse from "./section/TmpCourse.vue";
import TmpLearn from "./section/TmpLearn.vue";
import TmpMobile from "./section/TmpMobile.vue";
export default {
  components: {
    TmpHero,
    TmpDream,
    TmpCarrier,
    TmpInfo,
    TmpCourse,
    TmpLearn,
    TmpMobile,
  },
  name: "TmpMain",
};
</script>

<style lang="scss" scoped>
</style>


