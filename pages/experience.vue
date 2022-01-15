<template>
  <div class="main">
    <header>
      <nav>
        <div class="container">
          <div class="menu-line">
            <div class="line">
              <hr />
              <hr />
            </div>
          </div>
          <div class="logo">
            <img src="../assets/image/LOGO 1.svg" alt="" />
          </div>
          <div class="nav-book-button">
            <a class="btn btn-outline-white" href="./contact">BOOK NOW</a>
          </div>
        </div>
        <div class="social">
          <div class="container">
            <img
              class="icons"
              src="../assets/image/Icons/facebook.svg"
              alt=""
            />
            <img
              class="icons"
              src="../assets/image/Icons/instagram.svg"
              alt=""
            />
            <img class="icons" src="../assets/image/Icons/youtube.svg" alt="" />
          </div>
        </div>
      </nav>
    </header>
    <div class="fixed-button">
      <a class="btn btn-outline-white" href="./contact">BOOK NOW</a>
    </div>
    <section class="experience">
      <div class="container">
        <h2>Experience</h2>
        <div class="experi-desc">
          <h4>Unforgettable, Memorable experiences</h4>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisis
            tincidunt nisl elementum ultrices luctus habitasse. Ut orci nam
            lectus at massa enim elementum varius dictumst. Nulla a, sed enim
            turpis non lacinia fusce. Quis volutpat sit ullamcorper vitae magna
            vel sit pharetra scelerisque.
          </p>
        </div>
        <div class="experi-img">
          <img src="../assets/image/3D.svg" alt="" />
        </div>
      </div>
    </section>
    <section class="experience-links">
      <div class="container">
        <div class="destination-links"></div>
      </div>
    </section>
    <footer class="footer">
      <div class="container">
        <section class="footer-wrapper">
          <div class="footer-link-container">
            <div class="upper">
              <div class="desti">
                <h3 class="desti-title">Destination</h3>
                <ul class="desti-list">
                  <div>
                    <li class="footer-link"><a href="#">Bishoftu</a></li>
                    <li class="footer-link"><a href="#">Entoto</a></li>
                    <li class="footer-link"><a href="#">Awash</a></li>
                    <li class="footer-link"><a href="#">Water Park</a></li>
                    <li class="footer-link"><a href="#">Lake Tana</a></li>
                    <li class="footer-link"><a href="#"></a></li>
                  </div>

                  <div></div>
                </ul>
              </div>

              <div class="desti">
                <h3 class="desti-title">Wellness</h3>
                <ul class="desti-list">
                  <div>
                    <li class="footer-link"><a href="#">Spa</a></li>
                    <li class="footer-link"><a href="#">Pool</a></li>
                    <li class="footer-link"><a href="#">Massage</a></li>
                    <li class="footer-link"><a href="#">Manicure </a></li>
                    <li class="footer-link"><a href="#">Pedicure</a></li>
                    <li class="footer-link"><a href="#"></a></li>
                  </div>

                  <div></div>
                </ul>
              </div>

              <div class="desti">
                <h3 class="desti-title">Experience</h3>
                <ul class="desti-list">
                  <div>
                    <li class="footer-link"><a href="#">Kayaking</a></li>
                    <li class="footer-link"><a href="#">Archery</a></li>
                    <li class="footer-link"><a href="#">Cycling</a></li>
                    <li class="footer-link"><a href="#">Paintball </a></li>
                    <li class="footer-link"><a href="#">Horse Riding</a></li>
                    <li class="footer-link"><a href="#"></a></li>
                  </div>

                  <div></div>
                </ul>
              </div>

              <div class="desti">
                <h3 class="desti-title">Quick Links</h3>
                <ul class="desti-list">
                  <div>
                    <li class="footer-link"><a href="#">Home</a></li>
                    <li class="footer-link"><a href="#">Entoto</a></li>
                    <li class="footer-link"><a href="#">Our Story</a></li>
                    <li class="footer-link"><a href="#">Lake Tana </a></li>
                    <li class="footer-link"><a href="#">Awash</a></li>
                    <li class="footer-link"><a href="#"></a></li>
                  </div>

                  <div></div>
                </ul>
              </div>
            </div>
          </div>

          <div class="social">
            <h3 class="desti-title">follow us on</h3>

            <div class="icon-container">
              <img src="../assets/image/Icons/facebook.svg" alt="" />
              <img src="../assets/image/Icons/instagram.svg" alt="" />
              <img src="../assets/image/Icons/youtube.svg" alt="" />
            </div>
          </div>
        </section>

        <hr />
        <div class="lower">
          <img src="../assets/image/LOGO 1.svg" alt="" />
          <p>
            &copy; 2022. All Rights Reserved. Web Design & Development by
            <a href="https://versavvymedia.com/">Versavvy Media PLC</a>
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  data() {
    return {
      checkIn: "",
      checkOut: "",
      location: "",
      data: "",
    };
  },
  methods: {
    getData() {
      axios
        .post("http://localhost/reservation_system/book.php", {
          action: "fetchall",
        })
        .then((response) => {
          this.data = response.data;
        });
    },
  },
};
</script>

<style lang="scss" scoped>
.main {
  background: $kuriftu-white;
  header {
    background: url("../assets/image/exprience.jpg") rgba(0, 6, 27, 0.22)
      no-repeat;
    background-position: center center;
    background-size: cover;
    background-blend-mode: overlay;
    width: 100%;
    height: 90vh;
    z-index: -1;
    nav {
      .container {
        display: flex;
        align-items: flex-start;
        justify-content: space-between;
        .menu-line {
          margin-top: 1rem;
          .line {
            hr {
              margin: auto;
              margin-top: 1rem;
              color: $kuriftu-white;
              // height: 10rem;
              width: 2.35rem;
            }
          }
        }
        .logo {
          margin-top: 1rem;
          width: 9rem;
          @include responsive($md) {
            width: 11rem;
          }
        }
        .nav-book-button {
          display: none;
        }
      }
      .social {
        .container {
          display: grid;
          align-items: start;
          justify-items: center;
          margin-top: 13rem;
          @include responsive($md) {
            margin-top: 20rem;
          }

          .icons {
            margin-top: 2rem;
            width: 1.5rem;
          }
        }
      }
    }
  }
  @include responsive($lg) {
    header {
      nav {
        .container {
          align-items: center;

          .nav-book-button {
            margin-top: 1rem;

            display: block;
          }
        }
      }
    }
  }
  @include responsive($xl) {
    header {
      height: 100vh;
    }
  }
  .fixed-button {
    background: $kuriftu-black;
    position: fixed;
    width: 100%;

    height: 10vh;
    z-index: 9999;

    // display: grid;
    text-align: center;
    .btn {
      margin: 1.3rem;
    }
  }
  @include responsive($lg) {
    .fixed-button {
      display: none;
    }
  }
  .experience {
    margin-top: 6.25rem;
    .container {
      h2 {
        color: $kuriftu-brown;
        @extend .title;
        margin-top: 0.94rem;
        text-align: left;
      }
      .experi-desc {
        h4 {
          @extend .text;
          margin-top: 0.94rem;
          text-align: left;
          color: $kuriftu-grey;
        }
        p {
          @extend .text;
          margin-top: 0.94rem;
          text-align: left;
        }
      }
      .experi-img {
      }
    }
  }

  .experience-links {
    .container {
      .destination-links {
      }
    }
  }

  .footer {
    background: $kuriftu-black;
    margin-top: 6.25rem;

    .container {
      .footer-wrapper {
        .footer-link-container {
          .upper {
            display: grid;
            grid-template-columns: 1fr 1fr;
            place-items: center;

            .desti {
              .desti-title {
                color: $kuriftu-brown;
                @extend .title;
                margin-top: 4.37rem;
                text-align: center;
                font-size: 1rem;
                text-transform: uppercase;
              }
              .desti-list {
                text-align: center;
                margin-top: 1.88rem;
                margin-bottom: 1.88rem;
                // margin-left: 2rem;
                // gap: 3.31rem;
                div {
                  display: grid;
                  place-items: left;
                  gap: 1rem;
                  margin-top: 0.8rem;
                  .footer-link {
                    a {
                      color: $kuriftu-white;
                      font-size: 0.8rem;
                    }
                  }
                }
              }
            }
          }
        }
        .social {
          h3 {
            color: $kuriftu-brown;
            @extend .title;

            margin-top: 4.37rem;
            text-align: center;
            font-size: 1rem;
            text-transform: uppercase;
          }
          .icon-container {
            display: flex;
            justify-content: center;
            gap: 1.88rem;
            margin-top: 1.88rem;
            // width: 2rem;
          }
        }
      }
      hr {
        margin-top: 4.37rem;
        color: $kuriftu-brown;
      }
      .lower {
        display: grid;
        place-items: center;
        margin-top: 4.37rem;
        margin-bottom: 5rem;
        img {
          width: 10rem;
        }
        p {
          color: $kuriftu-white;
          font-size: 0.88rem;
          margin-top: 1.88rem;
          line-height: 1.3rem;
          text-align: center;
          a {
            color: $kuriftu-blue;
          }
        }
      }
    }
  }
  @include responsive($md) {
    .footer {
      .container {
        .footer-wrapper {
          .footer-link-container {
            .upper {
              display: grid;
              grid-template-columns: 1fr 1fr;
              place-items: center;

              .desti {
                .desti-title {
                  text-align: left;
                }
                .desti-list {
                  text-align: left;
                  margin-top: 0.98rem;
                  margin-bottom: 0.98rem;

                  div {
                    display: grid;
                    grid-template-columns: 1fr;
                    gap: 1.3rem;
                    margin-top: 0.98rem;
                    .footer-link {
                      a {
                        color: $kuriftu-white;
                        font-size: 1rem;
                        text-align: left;
                      }
                    }
                  }
                }
              }
            }
          }
        }

        .lower {
          margin-bottom: 6.3rem;
          img {
            width: 15rem;
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .footer {
      margin-top: 8.13rem;
      .container {
        .footer-wrapper {
          .footer-link-container {
            place-items: center;
            .upper {
              display: grid;
              grid-template-columns: 1fr 1fr 1fr 1fr;
              gap: 5rem;
              .desti {
                .desti-title {
                  text-align: left;
                }
                .desti-list {
                  text-align: left;
                  margin-top: 0.98rem;
                  margin-bottom: 0.98rem;
                }
              }
            }
          }
        }

        .lower {
          margin-bottom: 0rem;
          display: flex;
          justify-content: space-between;
          img {
            margin-bottom: 1rem;
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .footer {
      .container {
        .footer-wrapper {
          display: flex;
          justify-content: center;
          align-items: flex-start;
          gap: 8rem;
          .footer-link-container {
            .upper {
              gap: 8rem;
            }
          }
        }
      }
    }
  }
  @include responsive($xxl) {
    .footer {
      .container {
        .footer-wrapper {
          gap: 10rem;
          .footer-link-container {
            .upper {
              gap: 10rem;
            }
          }
        }
      }
    }
  }
}
</style>