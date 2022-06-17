<template>
  <main>
    <TmpHero />
    <TmpDream />
    <TmpCarrier />
    <TmpInfo />
    <TmpCourse />
    <TmpLearn />
    <TmpMobile />
    <TmpEvents />
    <TmpComment />
    <TmpRegister />
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
import TmpEvents from "./section/TmpEvents.vue";
import TmpComment from "./section/TmpComment.vue";
import TmpRegister from "./section/TmpRegister.vue";
export default {
  components: {
    TmpHero,
    TmpDream,
    TmpCarrier,
    TmpInfo,
    TmpCourse,
    TmpLearn,
    TmpMobile,
    TmpEvents,
    TmpComment,
    TmpRegister,
  },
  name: "TmpMain",
};
</script>

<style lang="scss" scoped>
</style>


