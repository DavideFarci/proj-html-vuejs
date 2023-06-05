<script>
export default {
  props: {
    devData: Array,
  },
};
</script>

<template>
  <div class="col-7">
    <div class="content">
      <div
        id="carouselExampleAutoplaying"
        class="carousel slide"
        data-bs-ride="carousel"
      >
        <div class="carousel-inner">
          <div class="carousel-item active">
            <div class="img-container">
              <img :src="`src/assets/img/${devData[0].image}`" alt="" />
              <i class="fa-solid fa-quote-left"></i>
            </div>
            <div>
              {{ devData[0].name }}
              <span>{{ devData[0].role }}</span>
            </div>
            <div>
              {{ devData[0].description }}
            </div>
            <div>
              <i style="color: #f9aa01" class="fa-solid fa-circle"></i>
              <i class="fa-solid fa-circle"></i>
              <i class="fa-solid fa-circle"></i>
            </div>
          </div>

          <div class="carousel-item">
            <div class="img-container">
              <img :src="`src/assets/img/${devData[1].image}`" alt="" />
              <i class="fa-solid fa-quote-left"></i>
            </div>
            <div>
              {{ devData[1].name }}<span> {{ devData[1].role }}</span>
            </div>
            <div>
              {{ devData[1].description }}
            </div>
            <div>
              <i class="fa-solid fa-circle"></i>
              <i style="color: #f9aa01" class="fa-solid fa-circle"></i>
              <i class="fa-solid fa-circle"></i>
            </div>
          </div>
          <div class="carousel-item">
            <div class="img-container">
              <img :src="`src/assets/img/${devData[2].image}`" alt="" />
              <i class="fa-solid fa-quote-left"></i>
            </div>
            <div>
              {{ devData[2].name }}
              <span>{{ devData[2].role }}</span>
            </div>
            <div>
              {{ devData[2].description }}
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
    .carousel-item span {
      color: #f9aa01;
    }
    .carousel-item > :nth-child(n + 2) {
      margin-bottom: 1rem;
    }

    .img-container {
      position: relative;
      margin: auto;
      height: 100px;
      width: 100px;
      // border-radius: 50%;
      // border: 4px solid #f9aa01;
      // overflow: hidden;
      margin-bottom: 1rem;
      img {
        border-radius: 50%;
        border: 4px solid #f9aa01;
      }
      .fa-quote-left {
        font-size: 1.1em;
        position: absolute;
        left: -12px;
        bottom: 61px;
        padding: 0.4rem;
        background-color: #f9aa01;
        border-radius: 50%;
      }
    }
    .fa-circle {
      font-size: 0.9em;
      margin-right: 0.5rem;
    }
  }
}
</style>
