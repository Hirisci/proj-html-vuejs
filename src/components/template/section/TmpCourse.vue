<template>
  <div class="wrapper-course">
    <TmpSectionSingle>
      <OListCourse>
        <template #header>
          <ASubTitle text="chose where you'd like to begin" />
          <ATitle
            class="class_title mt"
            text="Latest Featured"
            textColor="Courses"
          />
        </template>
        <template #footer>
          <AButton>
            <template #icon> View all courses </template>
            <FaS class="icon" icon="arrow-right-long" /> </AButton
        ></template>
      </OListCourse>
    </TmpSectionSingle>
  </div>
</template>

<script>
import OListCourse from "@/components/organism/OListCourse.vue";
import TmpSectionSingle from "../TmpSectionSingle.vue";
import AButton from "@/components/atom/AButton.vue";
import ATitle from "@/components/atom/ATitle.vue";
import ASubTitle from "@/components/atom/ASubTitle.vue";
export default {
  components: { OListCourse, TmpSectionSingle, AButton, ASubTitle, ATitle },
  nam: "TmpCourse",
};
</script>

<style lang="scss" scoped>
.wrapper-course {
  position: relative;
  &:after {
    display: block;
    content: "";
    position: absolute;
    z-index: -1;
    right: 0;
    left: 0;
    background-image: url("@/assets/screenshot/Untitled.svg");
    bottom: -190px;
    height: 100%;
    width: 100%;
  }
}
</style>