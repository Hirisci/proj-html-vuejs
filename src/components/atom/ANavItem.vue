<template>
  <li>{{ txt }} <FaS class="icon" v-if="openMenu" icon="angle-down" /></li>
</template>
<script>
export default {
  name: "ANavItem",
  props: {
    txt: String,
    openMenu: Boolean,
  },
};
</script>

<style lang="scss" scoped>
li {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: var(--p-sm);
  text-transform: capitalize;
  .icon {
    margin-top: 3px;
    font-size: 0.75rem;
  }
}
</style>