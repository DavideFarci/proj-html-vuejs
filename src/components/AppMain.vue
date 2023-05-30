<script>
export default {};
</script>

<template>
  <main>
    <div class="container">
      <!-- section piccola con 4 elementi in riga -->
      <section class="mini_sec">
        <div class="row">
          <div class="col-3">
            <div class="content"></div>
          </div>
          <div class="col-3">
            <div class="content"></div>
          </div>
          <div class="col-3">
            <div class="content"></div>
          </div>
          <div class="col-3">
            <div class="content"></div>
          </div>
        </div>
      </section>

      <!-- section con 2 col-6 (si ripete) -->
      <section class="duble">
        <div class="row">
          <div class="col-6">
            <div class="content"></div>
          </div>
          <div class="col-6">
            <div class="content"></div>
          </div>
        </div>
      </section>

      <!-- sezione con card -->
      <section class="special_category">
        <h2>Special Category</h2>
        <div class="row">
          <div class="col-4">
            <div class="content"></div>
          </div>
          <div class="col-4">
            <div class="content"></div>
          </div>
          <div class="col-4">
            <div class="content"></div>
          </div>
        </div>
      </section>

      <!-- carosello prodotti da ripetere = deal of the day -->
      <section class="carousel">
        <h2>Our Products</h2>
        <div class="row">
          <div class="col-2"><div class="content">Featured</div></div>
          <div class="col-2"><div class="content">New Arrival</div></div>
          <div class="col-2"><div class="content">Best Sellers</div></div>
        </div>
        <div class="row">
          <div class="col-3">
            <div class="content"></div>
          </div>
          <div class="col-3">
            <div class="content"></div>
          </div>
          <div class="col-3">
            <div class="content"></div>
          </div>
          <div class="col-3">
            <div class="content"></div>
          </div>
        </div>
      </section>

      <!-- altra sezione col-6 -->
      <section class="duble">
        <div class="row">
          <div class="col-6">
            <div class="content"></div>
          </div>
          <div class="col-6">
            <div class="content"></div>
          </div>
        </div>
      </section>

      <!-- secondo carosello -->
      <section class="carousel">
        <h2>Deal Of The Day</h2>
        <div class="row">
          <div class="col-2"><div class="content">1026 Days</div></div>
          <div class="col-2"><div class="content">13 Hours</div></div>
          <div class="col-2"><div class="content">24 Min</div></div>
          <div class="col-2"><div class="content">17 Sec</div></div>
        </div>
        <div class="row">
          <div class="col-3">
            <div class="content"></div>
          </div>
          <div class="col-3">
            <div class="content"></div>
          </div>
          <div class="col-3">
            <div class="content"></div>
          </div>
          <div class="col-3">
            <div class="content"></div>
          </div>
        </div>
      </section>
    </div>

    <!-- sezone a tutto schermo -->
    <section class="full_background">
      <div class="col-7">
        <div class="content"></div>
      </div>
    </section>

    <div class="container">
      <!-- sezione blog -->
      <section class="new_game_blogs">
        <h2>New Game Blog</h2>
        <div class="row">
          <div class="col-4">
            <div class="content"></div>
          </div>
          <div class="col-4">
            <div class="content"></div>
          </div>
          <div class="col-4">
            <div class="content"></div>
          </div>
        </div>
      </section>

      <!-- altra sezione piccola con 4 elementi in fila -->
      <section class="mini_sec_var">
        <div class="row">
          <div class="col-2">
            <div class="content"></div>
          </div>
          <div class="col-2">
            <div class="content"></div>
          </div>
          <div class="col-2">
            <div class="content"></div>
          </div>
          <div class="col-2">
            <div class="content"></div>
          </div>
          <div class="col-2">
            <div class="content"></div>
          </div>
        </div>
      </section>
    </div>
  </main>
</template>

<style lang="scss" scoped>
main {
  color: white;
  h2 {
    text-align: center;
    margin-bottom: 1.5rem;
  }
}
.mini_sec {
  margin-top: 3rem;
  .col-3 {
    padding: 1rem;
    height: 100%;
    .content {
      background-color: brown;
      height: 5rem;
    }
  }
}

.duble {
  margin-top: 3rem;
  .col-6 {
    padding: 1rem;
    height: 100%;
    .content {
      background-color: brown;
      height: 15rem;
    }
  }
}

.special_category {
  margin-top: 5rem;
  .col-4 {
    padding: 1rem;
    height: 100%;
    .content {
      background-color: brown;
      height: 24rem;
      aspect-ratio: 1 / 1;
    }
  }
}

.carousel {
  margin-top: 3rem;
  .row {
    justify-content: center;
    .col-2 {
      // margin: auto;
      border: 1px solid white;
      padding: 0;
      margin: 1.5rem 0;
      .content {
        padding: 0.9rem;
        text-align: center;
      }
    }
  }
  .col-3 {
    padding: 1rem;
    height: 17rem;
    .content {
      background-color: brown;
      height: 100%;
    }
  }
}

.full_background {
  height: 30rem;
  background-image: url(../assets/img/parallax.jpg);
  background-size: cover;
  background-position: bottom;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 3rem;
  .col-7 {
    background-color: rgba(252, 2, 2, 0.486);
    height: 20rem;
  }
}

.new_game_blogs {
  margin-top: 3rem;
  .col-4 {
    padding: 1rem;
    .content {
      background-color: brown;
      height: 17rem;
    }
  }
}

.mini_sec_var {
  margin-top: 3rem;
  .row {
    justify-content: center;
    .col-2 {
      padding: 1rem;
      height: 100%;
      .content {
        background-color: brown;
        height: 5rem;
      }
    }
  }
}
</style>
