<template>
  <section>
    <div :class="{ reverse: isReverse, center: isCenter }" class="container">
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
  },
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;

  &.reverse {
    flex-direction: row-reverse;
  }
  .content {
    width: 35%;
  }
  &.center {
    align-items: center;
  }
}
</style>