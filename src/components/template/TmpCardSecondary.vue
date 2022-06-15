<template>
  <div class="card">
    <img :src="require('@/assets/' + item.src)" alt="img" />
    <h4>{{ item.title }}</h4>
    <AText class="text" :text="item.text" />
    <a href="#"
      >Start now <span> <FaS class="icon" icon="arrow-right-long" /></span
    ></a>
  </div>
</template>

<script>
import AText from "../atom/AText.vue";
export default {
  components: { AText },
  name: "TmpCardSecondary",
  props: {
    item: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  align-items: center;
  justify-content: space-between;
  img {
    width: 10rem;
    height: 10rem;
  }
  .text {
    font-size: 1rem;
    line-height: 1.2rem;
  }
  a {
    text-decoration: none;
    vertical-align: center;
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 0.5rem;
    span {
      margin-top: 2.5px;
    }
  }
}
</style>