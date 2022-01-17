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
    <!-- <div class="fixed-button">
      <a class="btn btn-outline-white" href="./contact">BOOK NOW</a>
    </div> -->
    <section class="experience">
      <div class="container">
        <!-- <p>Unforgettable, Memorable experiences</p> -->
        <div class="experience-wrapper">
          <div class="experi-desc">
            <h2>Experience</h2>
            <h4>Unforgettable, Memorable experiences</h4>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisis
              tincidunt nisl elementum ultrices luctus habitasse. Ut orci nam
              lectus at massa enim elementum varius dictumst. Nulla a, sed enim
              turpis non lacinia fusce. Quis volutpat sit ullamcorper vitae
              magna vel sit pharetra scelerisque magna vel sit pharetra
              scelerisque.
            </p>
          </div>
          <div class="experi-img">
            <img src="../assets/image/3D.svg" alt="" />
          </div>
        </div>
      </div>
    </section>
    <section class="experience-links">
      <div class="container">
        <div class="destination-links">
          <ul>
            <li><a class="active" href="#">Entoto</a></li>
            <li><a href="#">Waterpark</a></li>
            <li><a href="#">Lake Tana</a></li>
            <li><a href="#">Awash</a></li>
          </ul>
        </div>
        <div class="exper-wrapper">
          <div class="exper-card">
            <div class="exper-img">
              <img src="../assets/image/entoto-exper.jpg" alt="" />
            </div>
            <div class="exper-title">
              <h3>Baking</h3>
            </div>
            <div class="exper-desc">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
              <div class="explore">
                <a href="#"
                  >EXPLORE
                  <hr
                /></a>
              </div>
            </div>
          </div>

          <div class="exper-card1">
            <div class="exper-img">
              <img src="../assets/image/entoto-exper2.jpg" alt="" />
            </div>
            <div class="exper-title">
              <h3>Rock ClImBing</h3>
            </div>
            <div class="exper-desc">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
              <div class="explore">
                <a href="#"
                  >EXPLORE
                  <hr
                /></a>
              </div>
            </div>
          </div>
        </div>
        <div class="exper-wrapper">
          <div class="exper-card">
            <div class="exper-img">
              <img src="../assets/image/entoto-exper3.jpg" alt="" />
            </div>
            <div class="exper-title">
              <h3>Paintball</h3>
            </div>
            <div class="exper-desc">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
              <div class="explore">
                <a href="#"
                  >EXPLORE
                  <hr
                /></a>
              </div>
            </div>
          </div>

          <div class="exper-card1">
            <div class="exper-img">
              <img src="../assets/image/entoto-exper4.jpg" alt="" />
            </div>
            <div class="exper-title">
              <h3>Horse Riding</h3>
            </div>
            <div class="exper-desc">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
              <div class="explore">
                <a href="#"
                  >EXPLORE
                  <hr
                /></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
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
      .experience-wrapper {
        .experi-desc {
          h2 {
            color: $kuriftu-brown;
            @extend .title;
            margin-top: 0.94rem;
            text-align: left;
          }
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
      }
    }
  }
  @include responsive($md) {
    .experience {
      .container {
        .experience-wrapper {
          display: flex;
          place-items: flex-end;
          // align-items: center;
          .experi-desc {
            width: 90%;

            background: $kuriftu-white;
            border-radius: 5rem;
            opacity: 0.6;
            z-index: 99;
            padding: 1rem;
            p {
              font-size: 0.8rem;
              line-height: 1.3rem;
              opacity: 100%;
            }
          }
          .experi-img {
            margin-left: -4rem;

            img {
              width: 50rem;
            }
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .experience {
      .container {
        .experience-wrapper {
          .experi-desc {
            width: 90%;
            border-radius: 7rem;
            padding: 0.5rem;
            p {
              font-size: 1rem;
              line-height: 1.75rem;
            }
          }
          .experi-img {
            margin-left: -5rem;
            img {
              width: 50rem;
            }
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .experience {
      .container {
        .experience-wrapper {
          .experi-desc {
            width: 60%;
            border-radius: 13rem;

            h4 {
              margin-top: 2.88rem;
              // padding: 1rem;
            }
            p {
              // margin-top: 2.88rem;
              font-size: 1.13rem;
              padding-right: 1rem;
            }
          }
          .experi-img {
            margin-left: -8rem;
            img {
              width: 45rem;
            }
          }
        }
      }
    }
  }
  .experience-links {
    margin-top: 6.25rem;
    .container {
      .destination-links {
        ul {
          display: flex;
          justify-content: center;
          gap: 1rem;
          li {
            a {
              @extend .title;
              font-size: 0.9rem;
              text-transform: uppercase;
              color: $kuriftu-grey;

              &:hover {
                color: $kuriftu-blue;
              }
              .active {
                color: $kuriftu-blue;
              }
            }
          }
        }
      }
      .exper-wrapper {
        display: grid;
        place-items: center;

        .exper-card,
        .exper-card1 {
          margin-top: 1.88rem;
          .exper-img {
            img {
              width: 20rem;
            }
          }
          .exper-title {
            background: $kuriftu-purple;
            padding: 0.8rem;
            width: 50%;
            min-width: 11.31rem;
            position: absolute;
            // bottom: 0;

            // margin-top: 15.2rem;
            margin-top: -3.23rem;

            h3 {
              color: $kuriftu-white;
              @extend .caps;
              font-size: 0.9rem;

              text-align: center;
            }
          }
          .exper-desc {
            width: 85%;
            background: #fff;
            padding: 1rem;
            p {
              @extend .text;

              color: $kuriftu-grey;
              font-size: 0.8rem;
              line-height: 1.3rem;
              text-align: left;
            }
            .explore {
              margin-top: 1rem;
              display: grid;
              place-items: left;
              a {
                font-size: 0.8rem;
                color: $kuriftu-grey;
                hr {
                  color: $kuriftu-grey;
                  width: 4rem;
                }
              }
            }
          }
        }
      }
    }
  }
  @include responsive($md) {
    .experience-links {
      .container {
        .destination-links {
          ul {
            gap: 2rem;
            li {
              a {
                font-size: 1rem;
              }
            }
          }
        }
        .exper-wrapper {
          display: flex;
          gap: 5rem;
          justify-content: center;
          .exper-card {
            .exper-title {
              width: 10%;
            }
          }
          .exper-card1 {
            margin-bottom: -10rem;
            .exper-title {
              width: 10%;
            }
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .experience-links {
      margin-top: 8.13rem;
      .container {
        .destination-links {
          ul {
            gap: 5rem;
          }
        }
        .exper-wrapper {
          // margin-left: 5rem;
          // margin-right: 5rem;
          gap: 3rem;

          .exper-card {
            margin-top: 4rem;
          }
          .exper-card1 {
            margin-top: 4rem;
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .experience-links {
      .container {
        .destination-links {
          ul {
            gap: 6rem;
          }
        }
        .exper-wrapper {
          // margin-left: 5rem;
          // margin-right: 5rem;
          gap: 10rem;

          .exper-card {
            margin-top: 4.88rem;
            .exper-img {
              img {
                width: 25rem;
              }
            }
            .exper-desc {
              width: 75%;
              p {
                font-size: 1rem;
              }
              .explore {
                a {
                  font-size: 1rem;
                  hr {
                    width: 5rem;
                  }
                }
              }
            }
          }
          .exper-card1 {
            margin-top: 4.88rem;
            .exper-img {
              img {
                width: 25rem;
              }
            }
            .exper-desc {
              width: 75%;
              p {
                font-size: 1rem;
              }
              .explore {
                a {
                  font-size: 1rem;
                  hr {
                    width: 5rem;
                  }
                }
              }
            }
          }
        }
      }
    }
  }
  @include responsive($xxl) {
    .experience-links {
      .container {
        .exper-wrapper {
          // margin-left: 5rem;
          // margin-right: 5rem;
          // gap: 6rem;
          margin-top: 6rem;
          .exper-card {
            .exper-img {
              img {
                width: 25rem;
              }
            }
          }
          .exper-card1 {
            .exper-img {
              img {
                width: 25rem;
              }
            }
          }
        }
      }
    }
  }
}
</style>