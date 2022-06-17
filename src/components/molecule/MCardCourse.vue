<template>
  <div class="card">
    <div class="card_img">
      <img :src="require('@/assets/img/' + course.src)" :alt="course.title" />
      <div class="card_price">{{ course.price }}</div>
    </div>
    <div class="card_author">
      <img
        class="card_author_img"
        :src="require('@/assets/img/' + course.author.img)"
        :alt="course.author.name"
      />
      <div class="card_author_name text">{{ course.author.name }}</div>
    </div>
    <div class="card_title">{{ course.title }}</div>
    <div class="card_info">
      <div class="card_info_lessons text">{{ course.lesson }} Lessons</div>
      <div class="card_info_students text">{{ course.person }} Students</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MCardCourse",
  props: {
    course: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  &_img {
    img {
      width: 100%;
      border-radius: 0.25rem;
    }
    position: relative;
    .card_price {
      position: absolute;
      top: 0;
      right: 0;
      padding: 0.75rem 1rem;
      background-color: var(--clr-primary);
      font-weight: 900;
      color: var(--clr-txt-1);
      border-radius: 0.25rem;
    }
  }
  &_author {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: var(--p-md);
    &_img {
      border-radius: 100%;
    }
  }
  &_title {
    padding: 0 var(--p-md);
    font-weight: 700;
    font-size: 1.25rem;
    letter-spacing: 0.1rem;
  }
  &_info {
    padding: var(--p-md);
    padding-top: var(--p-xl);
    display: flex;
    gap: 2rem;
  }
  .text {
    opacity: 0.75;
  }
}
</style>