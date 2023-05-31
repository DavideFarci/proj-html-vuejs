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
  <header id="header">
    <div class="container">
      <div class="pre_header">
        <div>
          <span class="wishlist">Wishlist(0)</span>
          <span class="help"
            >Need Help?<i class="fa-solid fa-chevron-down px-2 fs-6"></i
          ></span>
        </div>
        <div>Call 24/7 . 800-8754-987</div>
      </div>

      <div class="navigation">
        <img src="../assets/img/logo.png" alt="logo" />
        <AppNav :dataNav="this.navbar" />
        <div class="myAccount">
          <div class="i_search">
            <div class="regular"></div>
            <div class="hover"></div>
          </div>
          <div class="i_account">
            <div class="regular"></div>
            <div class="hover"></div>
          </div>
          <div class="i_cart">
            <div class="regular"></div>
            <div class="hover"></div>
          </div>
          <span class="cart_price">(0)£0.00</span>
        </div>
      </div>
    </div>
    <div class="jumbotron">
      <div class="over_text">
        <div class="yellow_strip">
          <span class="strip_content">Upcoming Stock</span>
        </div>
        <div class="title_content">
          <div>Far Cry 4</div>
          <div>Video Game</div>
        </div>
        <button>Shop Now</button>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  color: white;
  .pre_header {
    font-size: 0.9em;
    display: flex;
    justify-content: space-between;
    padding: 0.5rem;
    .wishlist {
      padding-right: 0.5rem;
      border-right: 1px solid #615a65;
    }
    .help {
      padding-left: 0.5rem;
      i:hover {
        cursor: pointer;
      }
    }
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
      .i_search {
        position: relative;
        .regular {
          position: relative;
          width: 40px;
          height: 40px;
          background-image: url(/src/assets/img/nav-icon.png);
          background-repeat: no-repeat;
          background-position-y: -64px;
          z-index: 10;
          &:hover {
            z-index: 0;
          }
        }
        .hover {
          cursor: pointer;
          width: 40px;
          height: 40px;
          background-image: url(/src/assets/img/nav-icon.png);
          background-repeat: no-repeat;
          background-position-y: 7px;
          position: absolute;
          bottom: 0;
          left: 0;
          z-index: 0;
          &:hover {
            z-index: 10;
          }
        }
      }
      .i_account {
        position: relative;
        .regular {
          position: relative;
          width: 40px;
          height: 40px;
          background-image: url(/src/assets/img/nav-icon.png);
          background-repeat: no-repeat;
          background-position-y: -206px;
          z-index: 10;
          &:hover {
            z-index: 0;
          }
        }
        .hover {
          cursor: pointer;
          width: 40px;
          height: 40px;
          background-image: url(/src/assets/img/nav-icon.png);
          background-repeat: no-repeat;
          background-position-y: -134px;
          position: absolute;
          bottom: 0;
          left: 0;
          z-index: 0;
          &:hover {
            z-index: 10;
          }
        }
      }
      .i_cart {
        position: relative;
        .regular {
          position: relative;
          width: 40px;
          height: 40px;
          background-image: url(/src/assets/img/nav-icon.png);
          background-repeat: no-repeat;
          background-position-y: -350px;
          z-index: 10;
          &:hover {
            z-index: 0;
          }
        }
        .hover {
          cursor: pointer;
          width: 40px;
          height: 40px;
          background-image: url(/src/assets/img/nav-icon.png);
          background-repeat: no-repeat;
          background-position-y: -278px;
          position: absolute;
          bottom: 0;
          left: 0;
          z-index: 0;
          &:hover {
            z-index: 10;
          }
        }
      }
      .cart_price {
        position: relative;
        color: #f9aa01;
        right: 25px;
        bottom: -11px;
        font-size: 0.9em;
      }
    }
  }
  .jumbotron {
    height: 37.125rem;
    // background-color: brown;
    background-image: url(../assets/img/Far-Cry-4-hidden-ending-Copia.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    align-items: center;
    .over_text {
      padding-left: 32rem;
      .yellow_strip {
        background-color: #f9aa01;
        width: 15rem;
        height: 2rem;
        transform: skew(-20deg);
        transform-origin: top right;
        overflow: hidden;
        margin-bottom: 4rem;
        // position: absolute;
        // right: 8rem;
        // top: 6rem;
        text-align: center;
        .strip_content {
          font-size: 1.9em;
          color: #242225;
          text-align: center;
          font-weight: bolder;
          position: relative;
          bottom: 6px;
        }
      }
      .title_content {
        font-size: 3em;
        font-weight: bolder;
        color: white;
        margin-bottom: 4rem;
        // position: absolute;
        // top: 8rem;
        // right: 6rem;
        & > * {
          letter-spacing: 2px;
        }
      }
      button {
        padding: 0.4rem 1.5rem;
        &:hover {
          background-color: #f9aa01;
        }
      }
    }
  }
}
</style>
