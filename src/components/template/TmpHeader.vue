<template>
  <header>
    <div class="container">
      <ALogo />
      <div>
        <ONavBar />
        <span class="notification">
          <FaS class="faIcon" icon="cart-shopping" />
        </span>
        <img class="faIcon" src="@/assets/img/circle-user-regular.svg" alt="" />
        <MSearchBar />
      </div>
    </div>
  </header>
</template>

<script>
import ALogo from "../atom/ALogo.vue";
import MSearchBar from "../molecule/MSearchBar.vue";
import ONavBar from "../organism/ONavBar.vue";
export default {
  components: { ALogo, ONavBar, MSearchBar },
  name: "TmpHeader",
};
</script>

<style lang="scss" scoped>
header {
  background-color: var(--clr-bg-header);
}
.container {
  height: var(--hgt-header);
  padding: var(--p-md);
  display: flex;
  align-items: center;
  justify-content: space-between;
  div {
    display: flex;
    align-items: center;
    gap: 1.5rem;
  }
}

.faIcon {
  margin-top: 4px;
  cursor: pointer;
  height: 1.2rem;
  font-size: 1.2rem;
}

.notification {
  position: relative;
  &::after {
    position: absolute;
    top: -5px;
    right: -10px;
    display: block;
    content: "0";
    background: var(--clr-primary);
    color: var(--clr-txt-1);
    font-size: 0.7rem;
    line-height: 0.7;
    text-align: center;
    padding: 0.25rem;
    height: 0.5rem;
    aspect-ratio: 1/1;
    border-radius: 100%;
  }
}
</style>