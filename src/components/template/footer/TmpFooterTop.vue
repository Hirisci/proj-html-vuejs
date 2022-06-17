<template>
  <div class="container">
    <div class="sx">
      <div>
        <MListFooter :obj="list[0]" />
      </div>
      <div class="social">
        <FaS
          class="icon"
          :icon="icon"
          v-for="(icon, idx) in social"
          :key="idx"
        />
      </div>
    </div>
    <div class="dx">
      <div>
        <MListFooter :obj="list[1]" />
      </div>
      <div>
        <MListFooter :obj="list[2]" />
      </div>
      <div>
        <MListFooter :obj="list[3]" />
      </div>
    </div>
  </div>
</template>

<script>
import MListFooter from "@/components/molecule/MListFooter.vue";
export default {
  components: { MListFooter },
  name: "TmpFooterTop",
  data() {
    return {
      social: [
        { prefix: "fab", iconName: "facebook-square" },
        { prefix: "fab", iconName: "twitter" },
        { prefix: "fab", iconName: "instagram" },
        { prefix: "fab", iconName: "linkedin" },
      ],
      list: [
        {
          text: "Address",
          list: [
            "382 NE 191st ST # 87394 Miami, FL 33179-3899",
            "+1(305) 547-9909(9am - 5pm EST, Monday-Friday)",
            "support@maxcoach.com",
          ],
        },
        {
          text: "Explore",
          list: ["Start here", "Blog", "About us"],
        },
        {
          text: "",
          list: ["Success Story", "Courses", "Contact us"],
        },
        {
          text: "Information",
          list: [
            "Membership",
            "Purchase Guide",
            "Privacy policy",
            "Terms of services",
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.social {
  display: flex;
  gap: 1rem;
  .icon {
    opacity: 0.5;
    &:hover {
      opacity: 1;
    }
  }
}
.container {
  display: flex;
  .sx {
    width: calc(100% / 2);
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  .dx {
    width: calc(100% / 3);
    display: flex;
    gap: 1rem;
    > * {
      width: calc(100% / 3);
      gap: 2rem;
      &:nth-child(2) {
        margin-top: 1rem;
      }
    }
  }
}
</style>