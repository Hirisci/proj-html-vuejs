<template>
  <div class="card">
    <div class="card_header">
      <slot name="header" />
    </div>
    <div>
      <slot name="body" />
    </div>
    <div>
      <slot name="footer" />
    </div>
  </div>
</template>

<script>
export default {
  name: "TmpCard",
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  > * {
    margin: var(--m-md) 0;
  }
}
</style>