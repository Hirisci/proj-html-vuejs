<template>
  <TmpSection :isReverse="true" class="mobile">
    <template #img>
      <div class="mobile_img">
        <img class="img-4" src="@/assets/img/maxcoach-shape-01.png" alt="" />
        <img class="img-1" src="@/assets/img/home-5-image-02.png" alt="" />
        <img
          class="img-2"
          src="@/assets/screenshot/underlay-shape-grey.svg"
          alt=""
        />
        <img class="img-3" src="@/assets/img/maxcoach-shape-07.png" alt="" />
      </div>
    </template>
    <TmpCard>
      <template #header>
        <ASubTitle text="what are you looking for?" />
        <ATitle class="mt" text="learn on your" textColor="mobile" />
        <ATitle class="mt" text="anytime!" />
      </template>
      <template #body>
        <AText
          text="save lessons for later and revise or write notes at any time and on multiple devices on your way. Never interfere with activities of enjoyment or other precious moments."
        />
      </template>
      <template #footer>
        <AButton> Download our App </AButton>
      </template>
    </TmpCard>
  </TmpSection>
</template>

<script>
import AButton from "@/components/atom/AButton.vue";
import ASubTitle from "@/components/atom/ASubTitle.vue";
import AText from "@/components/atom/AText.vue";
import ATitle from "@/components/atom/ATitle.vue";
import TmpCard from "../TmpCard.vue";
import TmpSection from "../TmpSection.vue";
export default {
  components: { AButton, ASubTitle, AText, ATitle, TmpCard, TmpSection },
  name: "TmpMobile",
};
</script>

<style lang="scss" scoped>
.mobile_img {
  display: flex;
  position: relative;
  align-items: center;
  .img-3 {
    z-index: -1;
    position: relative;
    top: 70px;
    right: 80px;
  }
  .img-2 {
    position: absolute;
    top: 60px;
    width: 70%;
    z-index: -2;
  }
  .img-4 {
    position: relative;
    left: -105px;
  }
}
</style>