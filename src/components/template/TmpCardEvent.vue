<template>
  <div class="card">
    <div class="card_text">
      <div class="card_position">
        <FaS icon="location-dot" />{{ obj.position }}
      </div>
      <div class="card_title">{{ obj.event }}</div>
    </div>
    <div class="card_info">
      <div class="card_day">{{ obj.day }}</div>
      <div class="card_month">{{ obj.month }}</div>
      <AButton class="card_btn">Get Ticket</AButton>
    </div>
  </div>
</template>

<script>
import AButton from "../atom/AButton.vue";
export default {
  components: { AButton },
  name: "TmpCardEvent",
  props: {
    obj: Object,
  },
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  justify-content: space-between;
  padding: var(--p-lg);
  background-color: var(--clr-bg-0);
  &_position {
    font-size: small;
    display: flex;
    gap: 0.5rem;
    opacity: 0.75;
  }
  &_title {
    margin-top: var(--m-md);
    font-size: 1.2rem;
    font-weight: 700;
    letter-spacing: 0.02rem;
  }
  &_text {
    width: 60%;
  }
  &_info {
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-self: flex-end;
  }
  &_btn {
    padding: 0.5rem 2rem;
  }
  &_day {
    font-size: 2.7rem;
    color: var(--clr-primary);
  }
  &_month {
    font-weight: bolder;
    text-transform: uppercase;
    font-size: 0.8rem;
    margin: var(--m-xs);
  }
}
</style>