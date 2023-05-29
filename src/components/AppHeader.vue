<script>
import AppNav from "./AppNav.vue";

export default {
  data() {
    return {
      navbar: [
        {
          title: "Home",
          link: "#",
          id: 1,
        },
        {
          title: "Shop",
          link: "#",
          id: 2,
        },
        {
          title: "Blog",
          link: "#",
          id: 3,
        },
        {
          title: "Media",
          link: "#",
          id: 4,
        },
        {
          title: "ShortCode",
          link: "#",
          id: 5,
        },
        {
          title: "Features",
          link: "#",
          id: 6,
        },
      ],
    };
  },
  components: { AppNav },
};
</script>

<template>
  <header>
    <div class="container">
      <div class="pre_header">
        <div>
          <span>Wishlist(0)</span>
          <span>Need Help?<i class="fa-solid fa-chevron-down"></i></span>
        </div>
        <div>Call 24/7 . 800-8754-987</div>
      </div>

      <div class="navigation">
        <img src="../assets/img/logo.png" alt="logo" />
        <AppNav :dataNav="this.navbar" />
        <div class="myAccount">
          <div><i class="fa-solid fa-magnifying-glass"></i></div>
          <div><i class="fa-regular fa-user"></i></div>
          <div><i class="fa-solid fa-bag-shopping"></i>(0)£0.00</div>
        </div>
      </div>
    </div>
    <div class="jumbotron"></div>
  </header>
</template>

<style lang="scss" scoped>
header {
  .pre_header {
    display: flex;
    justify-content: space-between;
    padding: 0.5rem;
  }
  .navigation {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 1rem;
    padding: 0.5rem;
    .myAccount {
      display: flex;
      gap: 1rem;
      padding: 0.5rem;
    }
  }
  .jumbotron {
    height: 42rem;
    background-color: brown;
  }
}
</style>
