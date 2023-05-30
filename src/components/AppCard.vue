<script>
export default {
  props: {
    cardInfo: Object,
  },
};
</script>

<template>
  <div class="col-4">
    <div class="content">
      <img :src="`src/assets/img/${cardInfo.image}`" :alt="cardInfo.name" />
      <div class="card_info">
        <div class="title">{{ cardInfo.name }}</div>
        <div class="shop">{{ cardInfo.shop }}</div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.col-4 {
  padding: 1rem;
  height: 100%;
  .content {
    position: relative;
    img {
      height: 100%;
      width: 100%;
    }
    .card_info {
      background-color: rgba(0, 0, 0, 0.377);
      position: absolute;
      bottom: 0;
      right: 0;
      left: 0;
    }
  }
}
</style>
