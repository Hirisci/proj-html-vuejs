<template>
  <div class="wrapper">
    <TmpSectionSingle :isColumn="true">
      <img class="img1" src="@/assets/img/maxcoach-shape-01.png" alt="" />
      <img class="img2" src="@/assets/img/maxcoach-shape-02.png" alt="" />

      <div class="title">
        <ATitle
          tag="h5"
          text="start today for getting"
          textColor="online certification"
        />
        <ATitle
          tag="h2"
          text="you can be your own guiding star with our help!"
        />
      </div>
      <AButton> Get started now</AButton>
    </TmpSectionSingle>
  </div>
</template>

<script>
import ATitle from "@/components/atom/ATitle.vue";
import TmpSectionSingle from "../TmpSectionSingle.vue";
import AButton from "@/components/atom/AButton.vue";
export default {
  components: { TmpSectionSingle, ATitle, AButton },
  name: "TmpRegister",
};
</script>

<style lang="scss" scoped>
.wrapper {
  background-color: var(--clr-bg-0);
  position: relative;
}

.img1 {
  position: absolute;
  left: 20%;
  top: 55%;
}
.img2 {
  position: absolute;
  right: 20%;
  top: 55%;
}
.title {
  text-align: center;
  margin: var(--m-lg);
}
</style>