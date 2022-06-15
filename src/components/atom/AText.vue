<template>
  <p>{{ text }}</p>
</template>

<script>
export default {
  name: "AText",
  props: {
    text: String,
  },
};
</script>

<style lang="scss" scoped>
p {
  opacity: 0.7;
  line-height: 2rem;
  font-size: 1.2rem;
}
</style>