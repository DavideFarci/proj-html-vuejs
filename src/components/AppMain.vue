<script>
import AppBlogCard from "./AppBlogCard.vue";
import AppCard from "./AppCard.vue";
import AppSlider from "./AppSlider.vue";

export default {
  data() {
    return {
      cards: [
        {
          id: 1,
          image: "category-image-01-446x550_t.jpg",
          name: "Batman",
          shop: "Shop Now",
        },
        {
          id: 2,
          image: "category-image-02-446x550_t.jpg",
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
    };
  },
  components: { AppCard, AppBlogCard, AppSlider },
};
</script>

<template>
  <main>
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
        <div class="row">
          <div class="col-6">
            <div class="content">
              <img src="../assets/img/cms-banner-01.jpg" alt="" />
              <div class="yellow_strip">
                <span class="strip_content">Most Popular</span>
              </div>
              <div class="title_content">
                <div>The Battelfield 4</div>
                <div>Naval Strike</div>
              </div>
            </div>
          </div>
          <div class="col-6">
            <div class="content">
              <img src="../assets/img/cms-banner-02.jpg" alt="" />
              <div class="yellow_strip">
                <span class="strip_content">Latest Game</span>
              </div>
              <div class="title_content">
                <div>Assasin's Creed</div>
                <div>Unity Game</div>
              </div>
            </div>
          </div>
        </div>
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
          <div class="col-2"><div class="content">Featured</div></div>
          <div class="col-2"><div class="content">New Arrival</div></div>
          <div class="col-2"><div class="content">Best Sellers</div></div>
        </div>
        <AppSlider :sliderData="this.cardsSlider" />
      </section>

      <!-- altra sezione col-6 -->
      <section class="double">
        <div class="row">
          <div class="col-6">
            <div class="content">
              <img src="../assets/img/cms-banner-03.jpg" alt="banner-03" />
              <div class="yellow_strip">
                <span class="strip_content">20% Discount</span>
              </div>
              <div class="title_content">
                <div>TDragon's Dogma</div>
                <div>Video Game</div>
              </div>
            </div>
          </div>
          <div class="col-6">
            <div class="content">
              <img src="../assets/img/cms-banner-04.jpg" alt="banner-04" />
              <div class="yellow_strip">
                <span class="strip_content">30% Discount</span>
              </div>
              <div class="title_content">
                <div>World of Tank</div>
                <div>New Game</div>
              </div>
            </div>
          </div>
        </div>
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
        <AppSlider :sliderData="this.cardsSlider" />
      </section>
    </div>

    <!-- sezone a tutto schermo -->
    <section class="full_background">
      <div class="col-7">
        <div class="content">
          <div class="quote"><i class="fa-solid fa-quote-left"></i></div>
          <img src="../assets/img/t5-1-100x100_left.jpg" alt="" />
          <div>Luies Charls<span>(Web Designer)</span></div>
          <div>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Optio
            exercitationem quam sunt suscipit voluptates quaerat aliquam
            officiis, porro voluptatibus ut sit quia quisquam sint, hic aperiam.
            Saepe, laboriosam! Provident, repellendus!
          </div>
          <div>
            <i class="fa-solid fa-circle"></i>
            <i class="fa-solid fa-circle"></i>
            <i class="fa-solid fa-circle"></i>
          </div>
        </div>
      </div>
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
  .col-6 {
    padding: 1rem;
    // height: 100%;
    .content {
      background-color: brown;
      position: relative;
      img {
        width: 100%;
      }
      //   height: 15rem;
    }
  }
  .yellow_strip {
    background-color: #f9aa01;
    width: 10rem;
    height: 1.5rem;
    transform: skew(-20deg);
    transform-origin: top right;
    overflow: hidden;
    position: absolute;
    right: 8rem;
    top: 6rem;
    text-align: center;
    .strip_content {
      font-size: 1.6em;
      color: #242225;
      text-align: center;
      font-weight: bolder;
      position: relative;
      bottom: 6px;
    }
  }
  .title_content {
    font-size: 1.6em;
    font-weight: bolder;
    color: white;
    position: absolute;
    top: 8rem;
    right: 6rem;
    & > * {
      letter-spacing: 2px;
    }
  }
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
  .col-7 {
    height: 20rem;
    text-align: center;
    padding: 1rem;
    .content {
      position: relative;
      & > * {
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
}

.new_game_blogs {
  margin-top: 3rem;
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
