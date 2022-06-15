<template>
  <header class="container">
    <ALogo />
    <div>
      <OrgNavBar />
      <FaS icon="cart-shopping" />
      <img class="faIcon" src="@/assets/img/circle-user-regular.svg" alt="" />
      <font-awesome-icon icon="fa-regular fa-circle-user" />
    </div>
  </header>
</template>

<script>
import ALogo from "../atom/ALogo.vue";
import OrgNavBar from "../organism/OrgNavBar.vue";
export default {
  components: { ALogo, OrgNavBar },
  name: "TmpHeader",
};
</script>

<style lang="scss" scoped>
header {
  height: var(--hgt-header);
  padding: var(--p-md);
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.faIcon {
  height: 1rem;
}
</style>