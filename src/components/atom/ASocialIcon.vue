<template>
  <Fas class="icon" :icon="text"></Fas>
</template>

<script>
export default {
  name: "ASocialIcon",
  props: {
    text: String,
  },
};
</script>

<style lang="scss" scoped>
.icon {
  height: 3rem;
  aspect-ratio: 1/1;
  opacity: 0.7;
  &:hover {
    opacity: 1;
  }
}
</style>