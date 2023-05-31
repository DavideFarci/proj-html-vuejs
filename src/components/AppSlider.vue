<script>
export default {
  props: {
    sliderData: Array,
  },
  computed: {
    convertedVote() {
      // NON FUNZIONA
      return Math.ceil((this.sliderData.rate / 10) * 5);
    },
  },
};
</script>

<template>
  <div id="carouselExample" class="carousel slide">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <div class="row">
          <div class="col-3" v-for="(card, i) in sliderData" :key="i">
            <div class="content">
              <img :src="`src/assets/img/${card.image}`" alt="" />
              <div class="product_info">
                <i
                  class="fa-regular fa-star"
                  v-for="star in 5"
                  :key="star"
                  :class="{
                    'fa-solid': star <= convertedVote,
                    'fa-star': star > convertedVote,
                  }"
                ></i>
                <div class="pro_name">{{ card.description }}</div>
                <div class="price">{{ card.price }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="carousel-item">
        <div class="row">
          <div class="col-3" v-for="(card, i) in sliderData" :key="i">
            <div class="content">
              <img :src="`src/assets/img/${card.image}`" alt="" />
              <div class="product_info">
                <i
                  class="fa-regular fa-star"
                  v-for="star in 5"
                  :key="star"
                  :class="{
                    'fa-solid': star <= convertedVote,
                    'fa-star': star > convertedVote,
                  }"
                ></i>
                <div class="pro_name">{{ card.description }}</div>
                <div class="price">{{ card.price }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="carousel-item">
        <div class="row">
          <div class="col-3" v-for="(card, i) in sliderData" :key="i">
            <div class="content">
              <img :src="`src/assets/img/${card.image}`" alt="" />
              <div class="product_info">
                <i
                  class="fa-regular fa-star"
                  v-for="star in 5"
                  :key="star"
                  :class="{
                    'fa-solid': star <= convertedVote,
                    'fa-star': star > convertedVote,
                  }"
                ></i>
                <div class="pro_name">{{ card.description }}</div>
                <div class="price">{{ card.price }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <button
      class="carousel-control-prev"
      type="button"
      data-bs-target="#carouselExample"
      data-bs-slide="prev"
    >
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button
      class="carousel-control-next"
      type="button"
      data-bs-target="#carouselExample"
      data-bs-slide="next"
    >
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>

<style lang="scss" scoped>
.row {
  justify-content: center;
}
// .fa-circle-left {
//   display: inline-block;
//   position: absolute;
//   left: 0;
//   bottom: 40%;
//   font-size: 1.4em;
//   cursor: pointer;
// }
// .fa-circle-right {
//   display: inline-block;
//   position: absolute;
//   left: 78.4rem;
//   bottom: 40%;
//   font-size: 1.4em;
//   cursor: pointer;
// }
.col-3 {
  padding: 1rem;
  .content {
    background-color: brown;
    img {
      width: 100%;
    }
    .product_info {
      background-color: #170e1f;
      .price:hover {
        display: none;
        z-index: 0;
      }
      .buttons {
        color: #f9aa01;
        button {
          display: none;
          background-color: #170e1f;
          color: white;
          width: calc(100% / 4);
          border: 1px solid #242225;
          font-size: 0.8em;
          padding: 0.1rem 0;
          &:hover {
            display: block;
            z-index: 10;
          }
        }
      }
    }
  }
}
</style>
