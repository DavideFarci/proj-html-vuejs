<script>
import AppBlogCard from "./AppBlogCard.vue";
import AppCard from "./AppCard.vue";
import AppCardDouble from "./AppCardDouble.vue";
import AppDevelopers from "./AppDevelopers.vue";
import AppSlider from "./AppSlider.vue";

export default {
  data() {
    return {
      cards: [
        {
          id: 1,
          image: "category-image-02-446x550_t.jpg",
          name: "Batman",
          shop: "Shop Now",
        },
        {
          id: 2,
          image: "category-image-01-446x550_t.jpg",
          name: "Bayonetta",
          shop: "Shop Now",
        },
        {
          id: 3,
          image: "category-image-03-446x550_t.jpg",
          name: "Dark Souls",
          shop: "Shop Now",
        },
      ],
      blogCards: [
        {
          image: "Nisi-ut-aliquid-ex-ea-com.jpg",
          date: "Jan 18,2021",
          comments: "0",
          description: "lorem ispsum dolor",
        },
        {
          image: "Illo-inventore-veritatis-quasi.jpg",
          date: "May 30,2021",
          comments: "12",
          description: "lorem ispsum dolor",
        },
        {
          image: "At-vero-eos-et-accusamus.jpg",
          date: "Apr 13,2021",
          comments: "3",
          description: "lorem ispsum dolor",
        },
      ],
      footerLinks: [
        {
          addressInfo: [
            {
              address: `60 29th Street San Francisco, CA 94110 507-Union Trade Center, United States of America`,
              mobile: `(+00) 123-456-789`,
              mail: `demo@example.com`,
            },
          ],
        },
        {
          information: [
            {
              name: "Bookmark",
              link: "#",
              id: 1,
            },
            {
              name: "Features",
              link: "#",
              id: 2,
            },
            {
              name: "Sitemap",
              link: "#",
              id: 3,
            },
            {
              name: "Lists",
              link: "#",
              id: 4,
            },
            {
              name: "Contact Us",
              link: "#",
              id: 5,
            },
          ],
        },
        {
          extras: [
            {
              name: "Delivery",
              link: "#",
              id: 1,
            },
            {
              name: "Cart",
              link: "#",
              id: 2,
            },
            {
              name: "Terms conditions",
              link: "#",
              id: 3,
            },
            {
              name: "My account",
              link: "#",
              id: 4,
            },
            {
              name: "About us",
              link: "#",
              id: 5,
            },
          ],
        },
      ],
      cardsSlider: [
        {
          ourProducts: [
            {
              image: "01-300x300.jpg",
              rate: 3,
              description: "Shopping Mahjong connect",
              price: "£100.00",
            },
            {
              image: "04-300x300.jpg",
              rate: 4,
              description: "Shopping Mahjong connect",
              price: "£100.00",
            },
            {
              image: "09-300x300.jpg",
              rate: 0,
              description: "Buddy and Lucky Solitair",
              price: "$83.90 - £90.00",
            },
            {
              image: "11-300x300.jpg",
              rate: 2,
              description: "Labirinths of the Worlf",
              price: "$110.00",
            },
          ],
          ourProductsNext: [
            {
              image: "12-300x300.jpg",
              rate: 4,
              description: "Shopping Mahjong connect",
              price: "£200.00",
            },
            {
              image: "08-300x300.jpg",
              rate: 1,
              description: "Shopping Mahjong connect",
              price: "£50.00",
            },
            {
              image: "05-300x300.jpg",
              rate: 5,
              description: "Buddy and Lucky Solitair",
              price: "$200.00 - £400.00",
            },
            {
              image: "15-300x300.jpg",
              rate: 2,
              description: "Labirinths of the Worlf",
              price: "$110.00",
            },
          ],
        },
        {
          dealProducts: [
            {
              image: "04-300x300.jpg",
              rate: 1,
              description: "Shopping Mahjong connect",
              price: "£150.00",
            },
            {
              image: "18-300x300.jpg",
              rate: 3,
              description: "Shopping Mahjong connect",
              price: "£90.00",
            },
            {
              image: "02-300x300.jpg",
              rate: 0,
              description: "Buddy and Lucky Solitair",
              price: "$83.90 - £90.00",
            },
            {
              image: "10-300x300.jpg",
              rate: 5,
              description: "Labirinths of the Worlf",
              price: "$190.00",
            },
          ],
        },
      ],
      partners: [
        {
          image: "t5-1-100x100_left.jpg",
          name: "Luies Charls",
          role: "(Web Designer)",
          description: `Lorem ipsum dolor sit amet consectetur, adipisicing elit. Optio
            exercitationem quam sunt suscipit voluptates quaerat aliquam
            officiis, porro voluptatibus ut sit quia quisquam sint, hic aperiam.
            Saepe, laboriosam! Provident, repellendus!`,
        },
        {
          image: "t2-1-100x100_left.jpg",
          name: "Luies Charls",
          role: "(Web Developer)",
          description: `Lorem ipsum dolor sit amet consectetur, adipisicing elit. Optio
            exercitationem quam sunt suscipit voluptates quaerat aliquam
            officiis, porro voluptatibus ut sit quia quisquam sint, hic aperiam.
            Saepe, laboriosam! Provident, repellendus!`,
        },
        {
          image: "t4-1-100x100_left.jpg",
          name: "Luies Charls",
          role: "(Team Menager)",
          description: `Lorem ipsum dolor sit amet consectetur, adipisicing elit. Optio
            exercitationem quam sunt suscipit voluptates quaerat aliquam
            officiis, porro voluptatibus ut sit quia quisquam sint, hic aperiam.
            Saepe, laboriosam! Provident, repellendus!`,
        },
      ],
      bigCards: [
        {
          image: "cms-banner-01.jpg",
          title: "Most Popular",
          descriptionUp: "The Battelfield 4",
          descriptionDown: "Naval Strike",
        },
        {
          image: "cms-banner-02.jpg",
          title: "Latest Game",
          descriptionUp: `Assasin's Creed`,
          descriptionDown: "Unity Game",
        },
        {
          image: "cms-banner-03.jpg",
          title: "20% Discount",
          descriptionUp: `TDragon's Dogma`,
          descriptionDown: "Video Game",
        },
        {
          image: "cms-banner-04.jpg",
          title: "30% Discount",
          descriptionUp: "World of Tank",
          descriptionDown: "New Game",
        },
      ],
    };
  },
  methods: {
    getLimitedArray(bigCards, start, end) {
      return bigCards.slice(start, end);
    },
  },
  components: { AppCard, AppBlogCard, AppSlider, AppDevelopers, AppCardDouble },
};
</script>

<template>
  <main>
    <a href="#header">
      <div class="square">
        <i class="fa-solid fa-chevron-up"></i>
      </div>
    </a>
    <div class="container">
      <!-- section piccola con 4 elementi in riga -->
      <section class="mini_sec">
        <div class="row">
          <div class="col-3">
            <div class="content">
              <div class="icon_delivery">
                <div class="standard"></div>
                <div class="hover"></div>
              </div>
              <div class="info">
                <div class="name fs-6 fw-bold">Free Shipping</div>
                <div class="details fs-6 text-dark-emphasis">
                  Free Shipping On All Order
                </div>
              </div>
            </div>
          </div>
          <div class="col-3">
            <div class="content">
              <div class="icon_money">
                <div class="standard"></div>
                <div class="hover"></div>
              </div>
              <div class="info">
                <div class="name fs-6 fw-bold">Free Shipping</div>
                <div class="details fs-6 text-dark-emphasis">
                  Free Shipping On All Order
                </div>
              </div>
            </div>
          </div>
          <div class="col-3">
            <div class="content">
              <div class="icon_member">
                <div class="standard"></div>
                <div class="hover"></div>
              </div>
              <div class="info">
                <div class="name fs-6 fw-bold">Free Shipping</div>
                <div class="details fs-6 text-dark-emphasis">
                  Free Shipping On All Order
                </div>
              </div>
            </div>
          </div>
          <div class="col-3">
            <div class="content">
              <div class="icon_policy">
                <div class="standard"></div>
                <div class="hover"></div>
              </div>
              <div class="info">
                <div class="name fs-6 fw-bold">Free Shipping</div>
                <div class="details fs-6 text-dark-emphasis">
                  Free Shipping On All Order
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- section con 2 col-6 (si ripete) -->
      <section class="double">
        <AppCardDouble :dataCard="this.getLimitedArray(bigCards, 0, 2)" />
      </section>

      <!-- sezione con card -->
      <section class="special_category">
        <h2 class="fs-1">Special Category</h2>
        <div class="row">
          <AppCard v-for="card in cards" :key="card.id" :cardInfo="card" />
        </div>
      </section>

      <!-- carosello prodotti da ripetere = deal of the day -->
      <section class="carousel">
        <h2 class="fs-1">Our Products</h2>
        <div class="row">
          <div class="col-2">
            <div style="color: #f9aa01" class="content">Featured</div>
          </div>
          <div class="col-2"><div class="content">New Arrival</div></div>
          <div class="col-2"><div class="content">Best Sellers</div></div>
        </div>
        <div class="row">
          <AppSlider :productsData="this.cardsSlider" />
        </div>
      </section>

      <!-- altra sezione col-6 -->
      <section class="double">
        <AppCardDouble :dataCard="this.getLimitedArray(bigCards, 2, 4)" />
      </section>

      <!-- secondo carosello -->
      <section class="carousel">
        <h2 class="fs-1">Deal Of The Day</h2>
        <div class="row">
          <div class="col-2"><div class="content">1026 Days</div></div>
          <div class="col-2"><div class="content">13 Hours</div></div>
          <div class="col-2"><div class="content">24 Min</div></div>
          <div class="col-2"><div class="content">17 Sec</div></div>
        </div>
        <!-- <AppSlider :dealData="this.cardsSlider.dealProducts" /> -->
      </section>
    </div>

    <!-- sezone a tutto schermo -->
    <section class="full_background">
      <AppDevelopers :devData="partners" />
    </section>

    <div class="container">
      <!-- sezione blog -->
      <section class="new_game_blogs">
        <h2 class="fs-1">New Game Blog</h2>
        <div class="row">
          <AppBlogCard v-for="blog in blogCards" :dataBlog="blog" />
        </div>
      </section>

      <!-- altra sezione piccola con 4 elementi in fila -->
      <section class="mini_sec_var">
        <div class="row">
          <div class="col-2">
            <div class="content">
              <img src="../assets/img/brand-01.png" alt="" />
            </div>
          </div>
          <div class="col-2">
            <div class="content">
              <img src="../assets/img/brand-02.png" alt="" />
            </div>
          </div>
          <div class="col-2">
            <div class="content">
              <img src="../assets/img/brand-03.png" alt="" />
            </div>
          </div>
          <div class="col-2">
            <div class="content">
              <img src="../assets/img/brand-04.png" alt="" />
            </div>
          </div>
          <div class="col-2">
            <div class="content">
              <img src="../assets/img/brand-05.png" alt="" />
            </div>
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
  .square {
    width: 40px;
    height: 40px;
    background-color: #000;
    transform: rotate(43deg);
    position: fixed;
    right: 19px;
    bottom: 50%;
    background-color: #f9aa01;
  }

  .fa-chevron-up {
    position: absolute;
    top: 31%;
    left: 30%;
    transform: rotate(-42deg);
    color: #fff;
  }
}
.mini_sec {
  margin-top: 3rem;
  .col-3 {
    padding: 1rem;
    height: 100%;
    .content {
      display: flex;
      align-items: center;
      gap: 1rem;
      // non aprire questi 4 (pericolo di morte!)
      .icon_delivery {
        position: relative;
        .standard {
          cursor: pointer;
          position: relative;
          z-index: 10;
          width: 60px;
          height: 50px;
          background-image: url(../assets/img/service-icon.png);
          background-repeat: no-repeat;
          background-position-y: -104px;
          z-index: 10;
          &:hover {
            z-index: 0;
          }
        }

        .hover {
          cursor: pointer;
          z-index: 0;
          width: 60px;
          height: 50px;
          background-image: url(../assets/img/service-icon.png);
          background-repeat: no-repeat;
          background-position-y: 11px;
          position: absolute;
          left: 0px;
          bottom: 2px;
          &:hover {
            z-index: 10;
          }
        }
      }
      .icon_money {
        position: relative;
        .standard {
          cursor: pointer;
          position: relative;
          z-index: 10;
          width: 60px;
          height: 50px;
          background-image: url(../assets/img/service-icon.png);
          background-repeat: no-repeat;
          background-position-y: -336px;
          z-index: 10;
          &:hover {
            z-index: 0;
          }
        }

        .hover {
          cursor: pointer;
          z-index: 0;
          width: 60px;
          height: 50px;
          background-image: url(../assets/img/service-icon.png);
          background-repeat: no-repeat;
          background-position-y: -220px;
          position: absolute;
          left: 0px;
          bottom: 2px;
          &:hover {
            z-index: 10;
          }
        }
      }
      .icon_member {
        position: relative;
        .standard {
          cursor: pointer;
          position: relative;
          z-index: 10;
          width: 60px;
          height: 50px;
          background-image: url(../assets/img/service-icon.png);
          background-repeat: no-repeat;
          background-position-y: -557px;
          z-index: 10;
          &:hover {
            z-index: 0;
          }
        }

        .hover {
          cursor: pointer;
          z-index: 0;
          width: 60px;
          height: 50px;
          background-image: url(../assets/img/service-icon.png);
          background-repeat: no-repeat;
          background-position-y: -442px;
          position: absolute;
          left: 0px;
          bottom: 2px;
          &:hover {
            z-index: 10;
          }
        }
      }
      .icon_policy {
        position: relative;
        .standard {
          cursor: pointer;
          position: relative;
          z-index: 10;
          width: 60px;
          height: 50px;
          background-image: url(../assets/img/service-icon.png);
          background-repeat: no-repeat;
          background-position-y: -786px;
          z-index: 10;
          &:hover {
            z-index: 0;
          }
        }

        .hover {
          cursor: pointer;
          z-index: 0;
          width: 60px;
          height: 50px;
          background-image: url(../assets/img/service-icon.png);
          background-repeat: no-repeat;
          background-position-y: -671px;
          position: absolute;
          left: 0px;
          bottom: 2px;
          &:hover {
            z-index: 10;
          }
        }
      }
    }
  }
}

.double {
  margin-top: 3rem;
}

.special_category {
  margin-top: 5rem;
  h2::after {
    content: "";
    display: block;
    height: 2px;
    width: 45px;
    background-color: #f9aa01;
    position: relative;
    left: 39rem;
    bottom: -5px;
  }
  .row {
    justify-content: center;
  }
}

.carousel {
  margin-top: 3rem;
  position: relative;
  h2::after {
    content: "";
    display: block;
    height: 2px;
    width: 45px;
    background-color: #f9aa01;
    position: relative;
    left: 39rem;
    bottom: -5px;
  }
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
}

.new_game_blogs {
  margin-top: 3rem;
  h2::after {
    content: "";
    display: block;
    height: 2px;
    width: 45px;
    background-color: #f9aa01;
    position: relative;
    left: 39rem;
    bottom: -5px;
  }
}

.mini_sec_var {
  margin-top: 3rem;
  .row {
    justify-content: center;
    .col-2 {
      padding: 1rem;
      height: 100%;
      padding: 2rem 0;
      border-top: 1px solid #37343a;
    }
  }
}
</style>

<!-- TODO: 
- Sistemare sezione double -->
