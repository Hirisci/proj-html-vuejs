<template>
  <section :class="{ wrapper: !isColumn }">
    <div class="container" :class="{ column: isColumn }">
      <slot />
    </div>
  </section>
</template>

<script>
export default {
  name: "TmpSectionSingle",
  props: {
    isColumn: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss" scoped>
.wrapper {
  background-color: var(--clr-bg-0);
}
.container {
  margin: auto;
  padding: var(--hgt-space-section) 0;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  &.column {
    flex-direction: column;
  }
}
</style>