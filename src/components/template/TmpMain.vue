<template>
  <main>
    <!-- hero -->
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
    <!-- fine hero -->
    <!-- section build you dream -->
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
    <!-- /section build you dream -->
    <!-- section carrier -->
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
    <!-- /section carrier -->
    <!-- section info -->
    <TmpSectionSingle>
      <ANumber number="1.926" text="finished sessions" />
      <ANumber number="3.092+" text="enrolled learners" />
      <ANumber number="200" text="online instructors" />
      <ANumber number="100%" text="satisfaction rate" />
    </TmpSectionSingle>
    <!-- /section info -->
    <!-- section course -->
    <TmpSectionSingle>
      <OListCourse>
        <template #header>
          <ASubTitle text="chose where you'd like to begin" />
          <ATitle
            class="class_title"
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
  </main>
</template>

<script>
import AButton from "../atom/AButton.vue";
import ASubTitle from "../atom/ASubTitle.vue";
import AText from "../atom/AText.vue";
import ATitle from "../atom/ATitle.vue";
import TmpCardSecondary from "./TmpCardSecondary.vue";
import TmpCard from "./TmpCard.vue";
import TmpSection from "./TmpSection.vue";
import OTabList from "../organism/OTabList.vue";
import TmpSectionSingle from "./TmpSectionSingle.vue";
import ANumber from "../atom/ANumber.vue";
import OListCourse from "../organism/OListCourse.vue";
export default {
  components: {
    TmpSection,
    TmpCard,
    ATitle,
    AText,
    AButton,
    ASubTitle,
    TmpCardSecondary,
    OTabList,
    TmpSectionSingle,
    ANumber,
    OListCourse,
  },
  name: "TmpMain",
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


