<template>
  <div class="hero-overlay">
    <TmpSection class="hero">
      <TmpCard class="hero_card">
        <template #header>
          <ATitle text="complete your" />
          <ATitle text="dreams in javaS" />
          <ATitle text="programming" />
        </template>
        <template #body
          ><AText
            text="Learn any coding program in distance and for a reasonable fee. You don't have to struggle alone, you've got our assistance help."
        /></template>
        <template #footer>
          <AButton>
            <template #icon>
              <FaS icon="download" />
            </template>
            Download free E-book
          </AButton>
        </template>
      </TmpCard>
      <template #img>
        <img src="@/assets/img/home-5-hero-image.png" alt="img" />
      </template>
    </TmpSection>
  </div>
</template>

<script>
import AButton from "../../atom/AButton.vue";
import AText from "../../atom/AText.vue";
import ATitle from "../../atom/ATitle.vue";
import TmpCard from "../TmpCard.vue";
import TmpSection from "../TmpSection.vue";

export default {
  name: "TmpHero",
  components: {
    TmpSection,
    TmpCard,
    ATitle,
    AText,
    AButton,
  },
};
</script>

<style lang="scss" scoped>
.hero {
  padding: var(--p-xl);
  &_card {
    margin-top: var(--m-xxl);
    width: 70%;
  }
}
.hero-overlay {
  width: 100%;
  position: relative;
  background-color: var(--clr-bg-header);
  z-index: -2;
  &:after {
    content: "";
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url("@/assets/screenshot/jumbo-overlay.svg");
    background-repeat: no-repeat;
    background-size: 100% 60%;
    transform: rotate(180deg);
    transform: scaleY(-1);
    z-index: -1;
  }
}
</style>