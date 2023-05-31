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
        <div class="more">
          <i class="fa-solid fa-plus"></i>
        </div>
        <div class="share">
          <i class="fa-solid fa-link"></i>
        </div>
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
    .img_container {
      position: relative;
      img {
        width: 100%;
        z-index: 10;
        &:hover {
          z-index: 0;
          opacity: 0.4;
        }
        &:hover .more,
        .share {
          visibility: visible;
          z-index: 10;
        }
      }
      .more {
        visibility: hidden;
        cursor: pointer;
        position: absolute;
        left: 38%;
        bottom: 41%;
        border: 1px solid white;
        aspect-ratio: 1/1;
        padding: 0.1rem;
        height: 38px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
      }
      .share {
        visibility: hidden;
        cursor: pointer;
        position: absolute;
        left: 51%;
        bottom: 41%;
        border: 1px solid white;
        aspect-ratio: 1/1;
        padding: 0.1rem;
        height: 38px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
      }
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
