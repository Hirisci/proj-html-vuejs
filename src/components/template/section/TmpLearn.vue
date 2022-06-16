<template>
  <TmpSection class="learn">
    <template #img>
      <div class="learn_img">
        <img class="img-1" src="@/assets/img/home-5-image-01.png" alt="" />
        <img
          class="img-2"
          src="@/assets/screenshot/underlay-shape-grey.svg"
          alt=""
        />
        <img class="img-3" src="@/assets/img/maxcoach-shape-05.png" alt="" />
      </div>
    </template>
    <TmpCard>
      <template #header>
        <ASubTitle text="why hesitate to register?" />
        <ATitle class="mt" text="Learn at your" />
        <ATitle class="mt" text="Own" textColor="Pace" />
      </template>
      <template #body>
        <OCheckList />
      </template>
      <template #footer>
        <AButton> Get started fro free </AButton>
      </template>
    </TmpCard>
  </TmpSection>
</template>

<script>
import ASubTitle from "@/components/atom/ASubTitle.vue";
import TmpCard from "../TmpCard.vue";
import TmpSection from "../TmpSection.vue";
import ATitle from "@/components/atom/ATitle.vue";
import OCheckList from "@/components/organism/OCheckList.vue";
import AButton from "@/components/atom/AButton.vue";
export default {
  components: { TmpSection, ASubTitle, ATitle, AButton, OCheckList, TmpCard },
  name: "TmpLearn",
};
</script>

<style lang="scss" scoped>
.learn {
  padding: var(--var-xl);
  margin: 8rem 0;
  &_img {
    position: relative;
    display: flex;
    align-items: center;
    .img-2 {
      z-index: -1;
      width: 70%;
      top: 25%;
      left: -12%;
      position: absolute;
    }
    .img-3 {
      z-index: -1;
      position: relative;
      top: 100px;
      left: -50px;
      border-radius: 100%;
    }
  }
}
</style>