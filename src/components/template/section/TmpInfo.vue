<template>
  <TmpSectionSingle>
    <ANumber number="1.926" text="finished sessions" />
    <ANumber number="3.092+" text="enrolled learners" />
    <ANumber number="200" text="online instructors" />
    <ANumber number="100%" text="satisfaction rate" />
  </TmpSectionSingle>
</template>

<script>
import ANumber from "@/components/atom/ANumber.vue";
import TmpSectionSingle from "../TmpSectionSingle.vue";
export default {
  components: { TmpSectionSingle, ANumber },
  name: "TmpInfo",
};
</script>

<style>
</style>