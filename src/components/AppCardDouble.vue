<script>
export default {
  props: {
    dataCard: Array,
  },
  filters: {
    limit(dataCard, count) {
      return dataCard.slice(0, count);
    },
  },
};
</script>

<template>
  <div class="row">
    <div class="col-6" v-for="(card, i) in dataCard | limit(2)" :key="i">
      <div class="content">
        <img :src="`../assets/img/${card.image}`" :alt="card.image" />
        <div class="yellow_strip">
          <span class="strip_content">{{ card.title }}</span>
        </div>
        <div class="title_content">
          <div>{{ card.descriptionUp }}</div>
          <div>{{ card.descriptionDown }}</div>
        </div>
      </div>
    </div>
    <!-- <div class="col-6">
      <div class="content">
        <img src="../assets/img/cms-banner-02.jpg" alt="" />
        <div class="yellow_strip">
          <span class="strip_content">Latest Game</span>
        </div>
        <div class="title_content">
          <div>Assasin's Creed</div>
          <div>Unity Game</div>
        </div>
      </div>
    </div> -->
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
</style>
