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
  <div id="carouselExample" class="carousel slide z-3">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <div class="row">
          <div class="col-3" v-for="(card, i) in sliderData" :key="i">
            <div class="content">
              <img :src="`src/assets/img/${card.image}`" alt="" />
              <div class="product_info">
                <div class="info_padding">
                  <i
                    class="fa-regular fa-star"
                    v-for="star in 5"
                    :key="star"
                    :class="{
                      'fa-solid': star <= convertedVote,
                      'fa-star': star > convertedVote,
                    }"
                  ></i>
                  <div class="pro_name fw-bolder">{{ card.description }}</div>
                  <div class="price">{{ card.price }}</div>
                </div>
                <div class="buttons">
                  <button><i class="fa-solid fa-bag-shopping"></i></button>
                  <button><i class="fa-solid fa-heart"></i></button>
                  <button><i class="fa-solid fa-maximize"></i></button>
                  <button><i class="fa-solid fa-eye"></i></button>
                </div>
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
                <div class="info_padding">
                  <i
                    class="fa-regular fa-star"
                    v-for="star in 5"
                    :key="star"
                    :class="{
                      'fa-solid': star <= convertedVote,
                      'fa-star': star > convertedVote,
                    }"
                  ></i>
                  <div class="pro_name fw-bolder">{{ card.description }}</div>
                  <div class="price">{{ card.price }}</div>
                </div>
                <div class="buttons">
                  <button><i class="fa-solid fa-bag-shopping"></i></button>
                  <button><i class="fa-solid fa-heart"></i></button>
                  <button><i class="fa-solid fa-maximize"></i></button>
                  <button><i class="fa-solid fa-eye"></i></button>
                </div>
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
                <div class="info_padding">
                  <i
                    class="fa-regular fa-star"
                    v-for="star in 5"
                    :key="star"
                    :class="{
                      'fa-solid': star <= convertedVote,
                      'fa-star': star > convertedVote,
                    }"
                  ></i>
                  <div class="pro_name fw-bolder">{{ card.description }}</div>
                  <div class="price">{{ card.price }}</div>
                </div>
                <div class="buttons">
                  <button><i class="fa-solid fa-bag-shopping"></i></button>
                  <button><i class="fa-solid fa-heart"></i></button>
                  <button><i class="fa-solid fa-maximize"></i></button>
                  <button><i class="fa-solid fa-eye"></i></button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <button
      class="carousel-control-prev z-1"
      type="button"
      data-bs-target="#carouselExample"
      data-bs-slide="prev"
    >
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button
      class="carousel-control-next z-1"
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
    cursor: pointer;
    img {
      width: 100%;
    }
    .product_info {
      .info_padding {
        background-color: #170e1f;
        padding: 0.5rem 0.5rem 0;
      }
      .fa-star {
        color: #f9aa01;
      }
      .price {
        font-size: 0.9em;
        color: #f9aa01;
      }
      .buttons {
        color: #f9aa01;
        button {
          display: none;
          background-color: #170e1f;
          color: white !important;
          width: calc(100% / 4);
          border: 1px solid #242225;
          font-size: 0.8em;
          padding: 0.1rem 0;
        }
      }
      &:hover .price {
        display: none;
      }
      &:hover .buttons button {
        display: inline-block;
      }
    }
  }
}

.carousel-inner {
  position: relative;
}
.carousel-control-next {
  position: absolute;
  right: -118px;
  top: 10rem;
  height: 50px;
  // z-index: 10;
}
.carousel-control-prev {
  position: absolute;
  left: -112px;
  top: 10rem;
  height: 50px;
  // z-index: 10;
}
// .carousel-control-prev-icon {
//   position: absolute;
//   left: -34px;
// }

// .carousel-control-next {
//   position: absolute;
//   right: -110px;
// }
</style>
