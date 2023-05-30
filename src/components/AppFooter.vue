<script>
export default {};
</script>

<template>
  <footer>
    <div class="container">
      <div class="footer_up">
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
      </div>
      <div class="footer_down">
        <div class="row">
          <div class="col-3">
            <div class="content"></div>
          </div>
          <div class="col-3">
            <div class="content"></div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  height: 30rem;
  background-image: url(../assets/img/footer-bg.png);
  display: flex;
  flex-direction: column;
  justify-content: end;
  .footer_up {
    padding: 1rem 0;
    .col-3 {
      padding: 1rem;
      .content {
        background-color: rgba(252, 2, 2, 0.486);
        height: 18rem;
      }
    }
  }
  .footer_down {
    padding: 0.5rem 0;
    margin-top: 2.5rem;
    .row {
      justify-content: space-between;
      .col-3 {
        pad: 0.5rem;
        .content {
          background-color: rgba(252, 2, 2, 0.486);
          height: 2rem;
        }
      }
    }
  }
}
</style>
