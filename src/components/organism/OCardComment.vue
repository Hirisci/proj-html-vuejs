<template>
  <div class="card">
    <div class="card_img">
      <img :src="require('@/assets/img/' + obj.img)" :alt="obj.name" />
    </div>
    <div class="card_comment">{{ obj.comment }}</div>
    <div class="card_name">{{ obj.name }}</div>
    <div class="card_position">/{{ obj.position }}</div>
  </div>
</template>

<script>
export default { name: "OCardComment", props: { obj: Object } };
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: var(--p-lg);
  align-items: center;
  gap: 1.5rem;
  background-color: #fff;
  z-index: 1;
  position: relative;
  padding-top: 4rem;
  -webkit-box-shadow: 0px 0px 15px -4px rgba(0, 0, 0, 0.25);
  box-shadow: 0px 0px 15px -4px rgba(0, 0, 0, 0.25);
  &_img {
    position: absolute;
    top: -4rem;
    z-index: 2;
    text-align: center;
    margin-bottom: 1rem;
    img {
      border-radius: 100%;
      width: 60%;
    }
  }
  &_comment {
    flex-grow: 1;
    line-height: 1.7rem;
    font-size: 1.2rem;
  }
  &_name {
    text-transform: uppercase;
    font-weight: 600;
  }
  &_position {
    opacity: 0.75;
    font-size: small;
  }
}
</style>