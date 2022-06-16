<template>
  <div v-show="isVisible">{{ text }}</div>
</template>

<script>
export default {
  name: "ATabBody",
  props: {
    text: String,
    isVisible: Boolean,
  },
};
</script>

<style lang="scss" scoped>
div {
  padding: var(--p-md);
  line-height: 1.5rem;
  opacity: 0.7;
}
</style>