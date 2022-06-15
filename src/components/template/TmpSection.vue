<template>
  <section>
    <div
      :class="{ reverse: isReverse, center: isCenter, column: isColumns }"
      class="container"
    >
      <div class="content">
        <slot />
      </div>
      <div class="img">
        <slot name="img"></slot>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TmpSection",
  props: {
    isReverse: {
      type: Boolean,
      default: false,
    },
    isCenter: {
      type: Boolean,
      default: false,
    },
    isColumns: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  justify-content: space-between;
  &.reverse {
    flex-direction: row-reverse;
  }

  &.center {
    align-items: center;
  }
  &.column {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 4rem;
  }
}
</style>