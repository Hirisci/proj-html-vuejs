<template>
  <component :is="tag">
    <span v-show="$slots.icon"><slot name="icon" /></span>
    <span>
      <slot />
    </span>
  </component>
</template>

<script>
export default {
  name: "AButton",
  props: {
    tag: { type: String, default: "button" },
  },
};
</script>

<style lang="scss" scoped>
button {
  padding: var(--p-md) var(--p-xxl);
  background-color: var(--clr-primary);
  font-weight: 600;
  color: var(--clr-txt-1);
  border: 1px solid var(--clr-txt-1);
  border-radius: 0.5rem;
  display: flex;
  gap: 1rem;
  cursor: pointer;
  z-index: 10;
  &:hover {
    background-color: var(--clr-secondary);
  }
}
</style>