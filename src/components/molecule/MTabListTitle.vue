<template>
  <div class="title" :class="{ active: isVisible }">
    <div>
      {{ title }}
    </div>
    <FaS class="icon" v-if="isVisible" icon="plus-circle" />
    <FaS class="icon" v-else icon="minus-circle" />
  </div>
</template>

<script>
export default {
  name: "MTabListTitle",
  props: {
    title: String,
    isVisible: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.title {
  display: flex;
  justify-content: space-between;
  font-size: 1.2rem;
  padding: var(--p-lg);
  font-weight: bold;
  border-radius: 0.5rem;
  &.active {
    color: var(--clr-txt-1);
    background-color: var(--clr-primary);
  }
  .icon {
    cursor: pointer;
  }
}
</style>