<template>
  <slot name="icon" />
  <component :is="tag"><slot /></component>
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
  border: 1px solid --clr-txt-1;
  border-radius: 0.5rem;
}
</style>