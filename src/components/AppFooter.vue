<script>
export default {
  data() {
    return {
      footerLinks: [
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
    };
  },
};
</script>

<template>
  <footer>
    <div class="footer_up">
      <div class="container">
        <div class="row">
          <div class="col-2">
            <div class="content">
              <ul>
                <h3>Address Info</h3>
                <li>
                  <i class="fa-solid fa-location-dot"></i>
                  60 29th Street San Francisco, CA 94110 507-Union Trade Center,
                  United States of America
                </li>
                <li>
                  <i class="fa-solid fa-phone"></i>
                  (+00) 123-456-789
                </li>
                <li>
                  <i class="fa-solid fa-envelope"></i>
                  demo@example.com
                </li>
              </ul>
            </div>
          </div>
          <div class="col-2">
            <div class="content">
              <ul>
                <h3>Address Info</h3>
                <li v-for="info in footerLinks[0].information" :key="info.id">
                  <a
                    onmouseover="this.style.color = '#f9aa01';"
                    onmouseout="this.style.color = 'grey';"
                    :href="info.link"
                    >{{ info.name }}</a
                  >
                </li>
              </ul>
            </div>
          </div>
          <div class="col-2">
            <div class="content">
              <ul>
                <h3>Address Info</h3>
                <li v-for="extra in footerLinks[1].extras" :key="extra.id">
                  <a
                    onmouseover="this.style.color = '#f9aa01';"
                    onmouseout="this.style.color = 'grey';"
                    :href="extra.link"
                    >{{ extra.name }}</a
                  >
                </li>
              </ul>
            </div>
          </div>
          <div class="col-4 offset-2">
            <div class="content">
              <h3>Our Newsletter</h3>
              <div>
                There ara many variations of passages of form humour or
                randomised
              </div>
              <div class="input_text">
                <input type="text" />
                <div class="send"></div>
                <div class="send_hover"></div>
              </div>

              <div class="social">
                <div><i class="fa-brands fa-facebook-f"></i></div>
                <div><i class="fa-brands fa-twitter"></i></div>
                <div><i class="fa-brands fa-google-plus-g"></i></div>
                <div><i class="fa-brands fa-skype"></i></div>
                <div><i class="fa-brands fa-instagram"></i></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer_down">
      <div class="container">
        <div class="row">
          <div class="col-3">
            <div class="content">
              Copyright <i class="fa-regular fa-copyright"></i> 2023 Codezeel
            </div>
          </div>
          <div class="col-3">
            <div class="content">
              <div class="am_ex"></div>
              <div class="discover"></div>
              <div class="masterC"></div>
              <div class="pay"></div>
              <div class="visa"></div>
            </div>
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
  margin: 0 0.5rem;
  .footer_up {
    padding: 1rem 0;
    .col-2 {
      padding: 0 1rem;
      .content {
        ul {
          list-style: none;
          color: grey;
          h3 {
            white-space: nowrap;
            font-size: 1.1em;
            color: white;
            margin-bottom: 1rem;
          }
          li {
            font-size: 0.9em;
            margin-bottom: 0.5rem;
            i {
              color: #f9aa01;
              margin-right: 0.5rem;
            }
            a {
              text-decoration: none;
              color: grey;
            }
          }
        }
      }
    }
    .col-4 {
      padding: 0 1rem;
      .content {
        height: 18rem;
        display: flex;
        flex-direction: column;
        gap: 1.5rem;
        padding: 0 1rem 1rem;
        color: gray;
        h3 {
          color: white;
        }
        .social {
          color: white;
          display: flex;
          gap: 1rem;
          i:hover {
            color: #f9aa01;
            cursor: pointer;
          }
        }
        .input_text {
          position: relative;
          display: flex;
          input {
            width: 19rem;
          }
          .send {
            height: 2rem;
            width: 2rem;
            background-image: url(/src/assets/img/newsletter.png);
            background-position-y: 8px;
            background-repeat: no-repeat;
            background-size: 19px;
            position: absolute;
            left: 17rem;
            bottom: -1px;
            z-index: 10;
            &:hover {
              z-index: 0;
            }
          }
          .send_hover {
            cursor: pointer;
            height: 2rem;
            width: 2rem;
            background-image: url(/src/assets/img/newsletter.png);
            background-position-y: -51px;
            background-repeat: no-repeat;
            background-size: 19px;
            position: absolute;
            left: 17rem;
            bottom: -1px;
            z-index: 0;
            &:hover {
              z-index: 10;
            }
          }
        }
      }
    }
  }
  .footer_down {
    padding: 0.5rem 0 0;
    margin-top: 2.5rem;
    border-top: 1px solid rgb(80, 80, 80);
    .row {
      justify-content: space-between;
      .col-3 {
        padding: 0.5rem;
        .content {
          display: flex;
          gap: 0.5rem;
          color: white;
          .am_ex {
            height: 26px;
            width: 43px;
            background-image: url(/src/assets/img/payments.png);
            background-repeat: no-repeat;
            background-position-y: -237px;
          }
          .discover {
            height: 26px;
            width: 43px;
            background-image: url(/src/assets/img/payments.png);
            background-repeat: no-repeat;
            background-position-y: -197px;
          }
          .masterC {
            height: 26px;
            width: 43px;
            background-image: url(/src/assets/img/payments.png);
            background-repeat: no-repeat;
            background-position-y: -76px;
          }
          .pay {
            height: 26px;
            width: 43px;
            background-image: url(/src/assets/img/payments.png);
            background-repeat: no-repeat;
            background-position-y: -116px;
          }
          .visa {
            height: 26px;
            width: 43px;
            background-image: url(/src/assets/img/payments.png);
            background-repeat: no-repeat;
            background-position-y: 0px;
          }
        }
      }
    }
  }
}
</style>
