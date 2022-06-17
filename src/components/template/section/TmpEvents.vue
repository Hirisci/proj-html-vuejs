<template>
  <div class="wrapper">
    <TmpSectionSingle :isColumn="true" class="events">
      <div class="title">
        <ASubTitle text="get in contact now" />
        <ATitle class="mt" text="Upcoming" textColor="Events" />
      </div>
      <div class="grid">
        <TmpCardEvent v-for="(card, idx) in lists" :key="idx" :obj="card" />
      </div>
      <div class="footer">
        <AText text="Exited about our event?" />
        <a href="#">View all events <FaS icon="right-long" /> </a>
      </div>
    </TmpSectionSingle>
  </div>
</template>

<script>
import ASubTitle from "@/components/atom/ASubTitle.vue";
import TmpSectionSingle from "../TmpSectionSingle.vue";
import ATitle from "@/components/atom/ATitle.vue";
import TmpCardEvent from "../TmpCardEvent.vue";
import AText from "@/components/atom/AText.vue";
export default {
  components: { TmpSectionSingle, ASubTitle, ATitle, TmpCardEvent, AText },
  name: "TmpEvents",
  data() {
    return {
      lists: [
        {
          position: "Texas, US",
          event: "Storytelling Workshop",
          day: 22,
          month: "Nov",
        },
        {
          position: "Ney York, US",
          event: "Painting Art Contest 2020",
          day: 10,
          month: "oct",
        },
        {
          position: "Hamburg, Germany",
          event: "International Art Fair 2020",
          day: 23,
          month: "Nov",
        },
        {
          position: "illinois, US",
          event: "Street Performance: Call for Artist",
          day: 15,
          month: "dec",
        },
        {
          position: "illinois, US",
          event: "Consumer Food Safety Education Conference",
          day: 22,
          month: "jul",
        },
        {
          position: "Dubai",
          event: "How meditation improve your mental health?",
          day: 12,
          month: "aug",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.title {
  text-align: center;
}
.events {
  display: flex;
  flex-direction: column;
}

.footer {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-weight: 700;
  a {
    color: var(--clr-primary);
  }
}
.grid {
  margin: var(--m-xxl) 0;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
}
.wrapper {
  position: relative;
  overflow: hidden;
  background-color: var(--clr-bg-0);
  z-index: -2;
  &:after {
    display: block;
    content: "";
    position: absolute;
    z-index: -1;
    top: 0;
    bottom: 0;
    right: -150px;
    left: 0;
    background-image: url("@/assets/screenshot/svg2.svg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: bottom right;
  }
}
</style>