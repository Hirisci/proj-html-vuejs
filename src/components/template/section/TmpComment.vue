<template>
  <div class="wrapper">
    <TmpSectionSingle :isColumn="true">
      <div class="title">
        <ASubTitle text="People are praising maxcoach" />
        <ATitle class="mt" text="what make they" textColor="love us?" />
      </div>
      <div class="comment">
        <OCardComment v-for="(card, idx) in list" :key="idx" :obj="card" />
      </div>
      <div class="bullet">
        <span></span>
        <span></span>
        <span></span>
        <span></span>
      </div>
    </TmpSectionSingle>
  </div>
</template>

<script>
import ASubTitle from "@/components/atom/ASubTitle.vue";
import TmpSectionSingle from "../TmpSectionSingle.vue";
import ATitle from "@/components/atom/ATitle.vue";
import OCardComment from "@/components/organism/OCardComment.vue";
export default {
  components: { TmpSectionSingle, ASubTitle, ATitle, OCardComment },
  name: "TmpComment",
  data() {
    return {
      list: [
        {
          img: "testimonial-avata-02.jpg",
          comment:
            "I am free to learn at my own pace, follow my own schedule and choose the subject i like. Great study portal for people like me.",
          name: "mina hollace",
          position: "Freelancer",
        },
        {
          img: "testimonial-avata-04.jpg",
          comment:
            "MaxCoach is my best choice. Their tutors are smart and professional when dealing with students",
          name: "madley pondor",
          position: "IT specialist",
        },
        {
          img: "testimonial-avata-01.jpg",
          comment:
            "I am happy with their arrangement of lessons and subjects. they reflect a scientific investigation",
          name: "luvic dubble",
          position: "Private Tutor",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.wrapper {
  background-color: var(--clr-bg-0);
}
.title {
  text-align: center;
  margin-bottom: 4rem;
}
.comment {
  display: flex;
  gap: 1rem;
  > * {
    width: calc((100% / 3) - 16px);
  }
}
.bullet {
  margin-top: var(--m-xxl);
  display: flex;
  gap: 1.5rem;
  span {
    opacity: 0.5;
    display: block;
    height: 0.5rem;
    aspect-ratio: 1/1;
    background-color: var(--clr-secondary);
    border-radius: 100%;
    &:first-child {
      opacity: 1;
      transform: scale(1.5);
    }
  }
}
</style>