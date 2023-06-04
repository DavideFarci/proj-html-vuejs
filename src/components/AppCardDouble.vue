<script>
export default {
  props: {
    dataCard: Array,
  },
};
</script>

<template>
  <div class="row">
    <div class="col-6" v-for="(card, i) in dataCard" :key="i">
      <div class="content">
        <img :src="`src/assets/img/${card.image}`" :alt="card.image" />
        <div class="yellow_strip">
          <span class="strip_content">{{ card.title }}</span>
        </div>
        <div class="title_content">
          <div>{{ card.descriptionUp }}</div>
          <div>{{ card.descriptionDown }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.col-6 {
  padding: 1rem;
  .content {
    background-color: brown;
    position: relative;
    img {
      width: 100%;
    }
  }
}

.yellow_strip {
  background-color: #f9aa01;
  width: 10rem;
  height: 1.5rem;
  transform: skew(-20deg);
  transform-origin: top right;
  overflow: hidden;
  position: absolute;
  right: 8rem;
  top: 6rem;
  text-align: center;
  .strip_content {
    font-size: 1.6em;
    color: #242225;
    text-align: center;
    font-weight: bolder;
    position: relative;
    bottom: 6px;
  }
}
.title_content {
  font-size: 1.6em;
  font-weight: bolder;
  color: white;
  position: absolute;
  top: 8rem;
  right: 6rem;
  & > * {
    letter-spacing: 2px;
  }
}
</style>
