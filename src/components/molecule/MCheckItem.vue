<template>
  <li>
    <FaS class="icon" icon="check" />
    <AText class="text" :text="text"></AText>
  </li>
</template>

<script>
import AText from "../atom/AText.vue";
export default {
  components: { AText },
  name: "MCheckItem",
  props: {
    text: String,
  },
};
</script>

<style lang="scss" scoped>
li {
  display: flex;
  align-items: center;
  gap: 1rem;
}
.icon {
  margin-top: 5px;
  color: var(--clr-primary);
}
</style>