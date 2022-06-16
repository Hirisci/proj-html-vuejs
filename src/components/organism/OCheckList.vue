<template>
  <ul>
    <MCheckItem v-for="(item, idx) in lists" :key="idx" :text="item" />
  </ul>
</template>

<script>
import MCheckItem from "../molecule/MCheckItem.vue";
export default {
  components: { MCheckItem },
  name: "OCheckList",
  data() {
    return {
      lists: [
        "Select & customize courses to your preferences",
        "Change the tutor and make arrangements",
        "Participate in events to join others",
        "get the desired certificate delivered at house",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>