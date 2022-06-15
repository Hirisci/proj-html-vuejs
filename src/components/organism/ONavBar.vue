<template>
  <ul>
    <ANavItem
      v-for="(item, idx) in items"
      :key="idx"
      :txt="item.txt"
      :openMenu="item.openMenu"
    />
  </ul>
</template>

<script>
import ANavItem from "../atom/ANavItem.vue";
export default {
  components: { ANavItem },
  name: "ONavBar",
  data() {
    return {
      items: [
        {
          txt: "home",
          openMenu: true,
        },
        {
          txt: "pages",
          openMenu: true,
        },
        {
          txt: "courses",
          openMenu: true,
        },
        {
          txt: "Features",
          openMenu: true,
        },
        {
          txt: "blog",
          openMenu: true,
        },
        {
          txt: "shop",
          openMenu: true,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
ul {
  display: flex;
  gap: var(--p-xl);
}
</style>