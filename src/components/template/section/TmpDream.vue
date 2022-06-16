<template>
  <TmpSection class="class" :isColumns="true">
    <ASubTitle text="start learning coding language" />
    <ATitle class="class_title" text="build your dream" textColor="TODAY" />
    <template #img>
      <div class="class_list">
        <TmpCardSecondary
          v-for="(card, idx) in cards"
          :key="idx"
          :item="card"
        />
      </div>
    </template>
  </TmpSection>
</template>

<script>
import ASubTitle from "@/components/atom/ASubTitle.vue";
import TmpSection from "../TmpSection.vue";
import ATitle from "@/components/atom/ATitle.vue";
import TmpCardSecondary from "../TmpCardSecondary.vue";
export default {
  components: { TmpSection, ASubTitle, ATitle, TmpCardSecondary },
  name: "TmpDream",
  data() {
    return {
      cards: [
        {
          src: "img/home-5-image-box-01.png",
          title: "Idea Discussion",
          text: "get teamed up with the specialist who work and teach coding for years at famous universities",
        },
        {
          src: "img/home-5-image-box-02.png",
          title: "Web development",
          text: "get teamed up with the specialist who work and teach coding for years at famous universities",
        },
        {
          src: "img/home-5-image-box-03.png",
          title: "System Administration",
          text: "get teamed up with the specialist who work and teach coding for years at famous universities",
        },
        {
          src: "img/home-5-image-box-04.png",
          title: "Graphic Design",
          text: "get teamed up with the specialist who work and teach coding for years at famous universities",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.class_list {
  display: flex;
  flex-direction: row;
  gap: 2rem;
}
.class {
  &_title {
    margin: var(--m-lg);
  }
}
</style>