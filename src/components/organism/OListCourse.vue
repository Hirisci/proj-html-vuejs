<template>
  <div class="course container">
    <div class="course_header">
      <slot name="header" />
    </div>
    <div class="course_body">
      <MCardCourse
        v-for="(course, idx) in courses"
        :key="idx"
        :course="course"
      />
    </div>
    <div class="course_footer">
      <slot name="footer" />
    </div>
  </div>
</template>

<script>
import MCardCourse from "../molecule/MCardCourse.vue";
export default {
  components: { MCardCourse },
  name: "OListCourse",
  data() {
    return {
      courses: [
        {
          author: {
            name: "Blanche Fields",
            img: "blanchefields.jpeg",
          },
          src: "course-01.jpg",
          title: "Learning to write as a professional author",
          price: "$40.00",
          lesson: 20,
          person: 50,
        },
        {
          author: {
            name: "Maggie Strickland",
            img: "maggiestrickland.jpeg",
          },
          src: "course-02.jpg",
          title: "Customer-centric info-Tech Strategies",
          price: "Free",
          lesson: 24,
          person: 769,
        },
        {
          author: {
            name: "Maggie Strickland",
            img: "maggiestrickland.jpeg",
          },
          src: "course-03.jpg",
          title: "Open Programming Courses for Everyone: Pyton",
          price: "$19.00",
          lesson: 17,
          person: 62,
        },
        {
          author: {
            name: "Blanche Fields",
            img: "blanchefields.jpeg",
          },
          src: "course-04.jpg",
          title: "Academic Listening and Note-taking",
          price: "$26.00",
          lesson: 14,
          person: 67,
        },
        {
          author: {
            name: "Blanche Fields",
            img: "blanchefields.jpeg",
          },
          src: "course-05.jpg",
          title: "Master jQuery in a Short Period of Time",
          price: "$39.00",
          lesson: 6,
          person: 51,
        },
        {
          author: {
            name: "Blanche Fields",
            img: "blanchefields.jpeg",
          },
          src: "course-06.jpg",
          title: "Introduction to Javascript for Beginners",
          price: "$59.00",
          lesson: 14,
          person: 76,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.course {
  position: relative;
  &_header {
    text-align: center;
    padding: var(--p-xl);
    padding-top: 0;
  }
  &_body {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 2rem;
  }
  &_footer {
    padding: var(--p-xl);
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>