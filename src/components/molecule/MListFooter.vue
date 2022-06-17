<template>
  <div><ATitle tag="h6" :text="obj.text" /></div>
  <ul>
    <li v-for="(li, idx) in obj.list" :key="idx">{{ li }}</li>
  </ul>
</template>

<script>
import ATitle from "../atom/ATitle.vue";

export default {
  components: { ATitle },
  name: "MlListFooter",
  props: {
    obj: Object,
  },
};
</script>



<style lang="scss" scoped>
ul {
  font-size: small;
}
li {
  margin: 0.75rem 0;
  opacity: 0.7;
  &:hover {
    opacity: 1;
  }
}
</style>