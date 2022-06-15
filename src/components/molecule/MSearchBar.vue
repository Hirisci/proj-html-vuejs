<template>
  <div class="search">
    <input class="search_input" type="text" placeholder="Search..." />
    <button class="search_btn"><FaS icon="magnifying-glass" /></button>
  </div>
</template>

<script>
export default {
  name: "MSearchBar",
};
</script>

<style lang="scss" scoped>
.search {
  border-radius: 0.5rem;
  padding: var(--p-md) var(--p-md);
  display: flex;
  gap: 0;
  background-color: #fff;
  &_input {
    width: 8rem;
    border: transparent;
    background-color: transparent;
  }
  &_btn {
    background-color: transparent;
    border: transparent;
    color: var(--clr-primary);
    font-size: 1.1rem;
  }
}
</style>