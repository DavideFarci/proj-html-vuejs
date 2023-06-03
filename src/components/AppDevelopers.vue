<script>
export default {
  props: {
    devData: {
      type: Array,
      required: true,
    },
  },
};
</script>

<template>
  <div class="col-7">
    <div class="content">
      <div
        v-if="partners && partners.length > 0"
        id="carouselExampleAutoplaying"
        class="carousel slide"
        data-bs-ride="carousel"
      >
        <div class="carousel-inner">
          <div class="carousel-item active">
            <div class="quote"><i class="fa-solid fa-quote-left"></i></div>
            <img :src="`src/assets/img/${partners[0].image}`" alt="" />
            <div>
              {{ partners[0].name }}
              <span>{{ partners[0].role }}</span>
            </div>
            <div>
              {{ partners[0].description }}
            </div>
            <div>
              <i style="color: #f9aa01" class="fa-solid fa-circle"></i>
              <i class="fa-solid fa-circle"></i>
              <i class="fa-solid fa-circle"></i>
            </div>
          </div>
          <div class="carousel-item">
            <div class="quote"><i class="fa-solid fa-quote-left"></i></div>
            <img :src="`src/assets/img/${partners[1].image}`" alt="" />
            <div>
              {{ partners[1].name }}<span> {{ partners[1].role }}</span>
            </div>
            <div>
              {{ partners[1].description }}
            </div>
            <div>
              <i class="fa-solid fa-circle"></i>
              <i style="color: #f9aa01" class="fa-solid fa-circle"></i>
              <i class="fa-solid fa-circle"></i>
            </div>
          </div>
          <div class="carousel-item">
            <div class="quote"><i class="fa-solid fa-quote-left"></i></div>
            <img :src="`src/assets/img/${partners[2].image}`" alt="" />
            <div>
              {{ partners[2].name }}
              <span>{{ partners[2].role }}</span>
            </div>
            <div>
              {{ partners[2].description }}
            </div>
            <div>
              <i class="fa-solid fa-circle"></i>
              <i class="fa-solid fa-circle"></i>
              <i style="color: #f9aa01" class="fa-solid fa-circle"></i>
            </div>
          </div>
        </div>
        <button
          class="carousel-control-prev"
          type="button"
          data-bs-target="#carouselExampleAutoplaying"
          data-bs-slide="prev"
        >
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button
          class="carousel-control-next"
          type="button"
          data-bs-target="#carouselExampleAutoplaying"
          data-bs-slide="next"
        >
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.col-7 {
  height: 20rem;
  text-align: center;
  padding: 1rem;
  .content {
    position: relative;
    .carousel-item span {
      color: #f9aa01;
    }
    .carousel-item > :nth-child(n + 2) {
      margin-bottom: 1rem;
    }

    .fa-quote-left {
      padding: 0.3rem;
      background-color: #f9aa01;
      border-radius: 50%;
      position: absolute;
      left: 32.5rem;
      top: 1.3rem;
    }
    img {
      border-radius: 50%;
      border: 4px solid #f9aa01;
    }
    .fa-circle {
      font-size: 0.9em;
      margin-right: 0.5rem;
    }
  }
}
</style>
