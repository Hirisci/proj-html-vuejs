<template>
  <TmpSection class="carrier" :isReverse="true">
    <template #img>
      <div class="carrier_img">
        <img
          class="carrier_img_one"
          src="@/assets/screenshot/underlay-shape-lilla.svg"
          alt=""
        />
        <img
          class="carrier_img_two"
          src="@/assets/img/about-us-03-image-01.png"
          alt=""
        />
      </div>
    </template>
    <div class="carrier_content">
      <ASubTitle text="Dream with maxCoach" />
      <div class="carrier_content-title">
        <ATitle text="construct a " textColor="stunning" />
        <ATitle text="career perspective" />
      </div>
      <div class="carrier_content-body">
        <OTabList />
      </div>
    </div>
  </TmpSection>
</template>

<script>
import ASubTitle from "@/components/atom/ASubTitle.vue";
import TmpSection from "../TmpSection.vue";
import ATitle from "@/components/atom/ATitle.vue";
import OTabList from "@/components/organism/OTabList.vue";
export default {
  components: { TmpSection, ASubTitle, ATitle, OTabList },
  name: "TmpCarrier",
};
</script>

<style lang="scss" scoped>
.carrier {
  &_img {
    position: relative;
    &_one {
      position: absolute;
      z-index: -1;
      top: 20%;
      left: rem;
      height: 22rem;
    }
    &_two {
      position: relative;
      right: -6.25rem;
    }
  }
  &_content-title {
    margin: var(--m-lg) 0;
    > * {
      margin-bottom: var(--m-md);
    }
  }
}
</style>