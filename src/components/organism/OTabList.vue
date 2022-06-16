<template>
  <div class="tab" v-for="(tab, idx) in tabs" :key="idx">
    <MTabListTitle
      :title="tab.title"
      :isVisible="tab.isActive"
      @btn-click="changeActive()"
    />
    <ATabBody :isVisible="tab.isActive" :text="tab.body" />
  </div>
</template>

<script>
import ATabBody from "../atom/ATabBody.vue";
import MTabListTitle from "../molecule/MTabListTitle.vue";
export default {
  components: { MTabListTitle, ATabBody },
  name: "OTabList",
  data() {
    return {
      tabs: [
        {
          title: "Multiple platforms supported for teaching & Studying",
          isActive: true,
          body: "MacCoach support the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren't supposed to be devoured in a shot time, you can always access our knowledge base from any device ",
        },
        {
          title: "Multiple platforms supported for teaching & Studying",
          isActive: false,
          body: "MacCoach support the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren't supposed to be devoured in a shot time, you can always access our knowledge base from any device ",
        },
        {
          title: "Multiple platforms supported for teaching & Studying",
          isActive: false,
          body: "MacCoach support the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren't supposed to be devoured in a shot time, you can always access our knowledge base from any device ",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.tab {
  -webkit-box-shadow: 0px 0px 15px -4px rgba(0, 0, 0, 0.42);
  box-shadow: 0px 0px 15px -4px rgba(0, 0, 0, 0.42);
  margin: var(--m-lg) 0;
  &:first-of-type {
    margin-top: 3rem;
  }
}
</style>