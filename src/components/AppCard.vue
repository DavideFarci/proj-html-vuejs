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
    cursor: pointer;
    img {
      height: 100%;
      width: 100%;
    }
    .card_info {
      background-color: rgba(0, 0, 0, 0.377);
      padding: 1rem;
      position: absolute;
      bottom: 0;
      right: 0;
      left: 0;
      .title {
        font-size: 1.1em;
        font-weight: bolder;
        margin-bottom: 0.5rem;
      }
      .shop {
        color: #f9aa01;
        &:hover {
          text-decoration: underline;
          cursor: pointer;
        }
      }
    }
    &:hover .card_info {
      background-color: rgba(0, 0, 0, 1);
    }
  }
}
</style>
