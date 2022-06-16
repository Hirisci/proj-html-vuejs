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
    <div class="wrapper-course">
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
    </div>
    <!-- /section course -->
    <!-- section learn pace -->
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
    <!-- /section learn pace -->
    <!-- section mobile -->
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
    <!-- /section mobile -->
    <!-- section mobile -->
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
import OCheckList from "../organism/OCheckList.vue";
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
    OCheckList,
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
.mt {
  margin-top: var(--m-md);
}
</style>


