<script>
export default {
  props: {
    productsData: Array,
  },
  // computed: {
  //   convertedVote() {
  //     // NON FUNZIONA
  //     return Math.ceil((card.rate / 10) * 5);
  //   },
  // },
  // computed: {
  //   convertedVote() {
  //     return this.sliderData.map((card) => {
  //       return Math.ceil((card.rate / 10) * 5);
  //     });
  //   },
  // },
  computed: {
    convertedVote() {
      const allCards = [
        ...this.productsData.ourProducts,
        ...this.productsData.ourProductsNext,
      ];
      return allCards.map((card) => {
        return Math.ceil((card.rate / 10) * 5);
      });
    },
  },
};
</script>

<template>
  <div id="carouselExample" class="carousel slide z-3">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <div class="row">
          <template>
            <div
              class="col-3"
              v-for="(card, i) in productsData.ourProducts"
              :key="i"
            >
              <div class="content">
                <img :src="`src/assets/img/${card.image}`" alt="" />
                <div class="product_info">
                  <div class="info_padding">
                    <i
                      class="fa-regular fa-star"
                      v-for="star in 5"
                      :key="star"
                      :class="{
                        'fa-solid': star <= convertedVote[i],
                        'fa-star': star > convertedVote[i],
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
          </template>
        </div>
      </div>
      <div class="carousel-item">
        <div class="row">
          <template>
            <div
              class="col-3"
              v-for="(secondCard, i) in productsData.ourProductsNext"
              :key="i"
            >
              <div class="content">
                <img :src="`src/assets/img/${secondCard.image}`" alt="" />
                <div class="product_info">
                  <div class="info_padding">
                    <i
                      class="fa-regular fa-star"
                      v-for="star in 5"
                      :key="star"
                      :class="{
                        'fa-solid': star <= convertedVote[i],
                        'fa-star': star > convertedVote[i],
                      }"
                    ></i>
                    <div class="pro_name fw-bolder">
                      {{ secondCard.description }}
                    </div>
                    <div class="price">{{ secondCard.price }}</div>
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
          </template>
        </div>
      </div>
    </div>
    <!-- controllo scorrimento SX -->
    <button
      class="carousel-control-prev z-1"
      type="button"
      data-bs-target="#carouselExample"
      data-bs-slide="prev"
    >
      <!-- <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span> -->
      <i class="fa-regular fa-circle-left"></i>
    </button>
    <!-- controllo scorrimento DX -->
    <button
      class="carousel-control-next z-1"
      type="button"
      data-bs-target="#carouselExample"
      data-bs-slide="next"
    >
      <!-- <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span> -->
      <i class="fa-regular fa-circle-right"></i>
    </button>
  </div>
</template>

<style lang="scss" scoped>
.col-3 {
  padding: 1rem;

  .row {
    justify-content: center;
  }

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
  .fa-circle-right {
    font-size: 1.7rem;
    cursor: pointer;
  }
}
.carousel-control-prev {
  position: absolute;
  left: -112px;
  top: 10rem;
  height: 50px;
  .fa-circle-left {
    font-size: 1.7rem;
    cursor: pointer;
  }
}
</style>
