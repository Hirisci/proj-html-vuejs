<template>
  <section class="wrapper">
    <div class="container">
      <slot />
    </div>
  </section>
</template>

<script>
export default {
  name: "TmpSectionSingle",
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
}
</style>