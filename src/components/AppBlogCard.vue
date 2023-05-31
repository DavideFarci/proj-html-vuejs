<script>
export default {
  props: {
    dataBlog: Object,
  },
};
</script>

<template>
  <div class="col-4">
    <div class="content">
      <div class="img_container">
        <img :src="`src/assets/img/${dataBlog.image}`" :alt="dataBlog.image" />
      </div>
      <div class="info_blog">
        <div class="d-flex justify-content-between px-2">
          <div>
            <span style="margin-right: 0.5rem"
              ><i class="fa-regular fa-calendar-days"></i
            ></span>
            <span>{{ dataBlog.date }}</span>
          </div>
          <div>
            <span style="margin-right: 0.5rem"
              ><i class="fa-solid fa-comments"></i
            ></span>
            <span>{{ dataBlog.comments }} comments</span>
          </div>
        </div>
        <div class="description px-2">
          {{ dataBlog.description }}
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.col-4 {
  padding: 1rem;
  .content {
    img {
      width: 100%;
    }
    .info_blog {
      background-color: #170e1f;
      padding: 0.5rem;
      span {
        font-size: 0.9em;
        font-weight: bold;
      }
      i {
        color: #f9aa01;
        font-size: 0.9em;
      }
    }
  }
}
</style>
