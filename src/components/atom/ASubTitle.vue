<template>
  <p>{{ text }}</p>
</template>

<script>
export default {
  name: "ASubTitle",
  props: {
    text: String,
  },
};
</script>

<style lang="scss" scoped>
p {
  text-transform: uppercase;
  font-size: small;
  letter-spacing: 0.1rem;
}
</style>