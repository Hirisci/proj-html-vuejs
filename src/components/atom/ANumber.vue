<template>
  <div class="card">
    <div class="card_number">{{ number }}</div>
    <div class="card_text">{{ text }}</div>
  </div>
</template>

<script>
export default {
  name: "ANumber",
  props: {
    number: String,
    text: String,
  },
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  text-align: center;
  &_number {
    font-size: 2rem;
    font-weight: 900;
    color: var(--clr-primary);
  }
  &_text {
    text-transform: uppercase;
    font-size: small;
    font-weight: 900;
  }
}
</style>