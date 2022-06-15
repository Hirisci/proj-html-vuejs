<template>
  <component class="title" :is="tag">
    {{ text }} <span v-if="textColor">{{ textColor }}</span>
  </component>
</template>

<script>
export default {
  name: "ATitle",
  props: {
    tag: {
      type: String,
      default: "h1",
    },
    text: String,
    textColor: String,
  },
};
</script>

<style lang="scss" scoped>
.title {
  font-weight: 600;
  text-transform: capitalize;
  letter-spacing: 1px;
}
span {
  font-weight: 400;
  color: var(--clr-primary);
}
</style>