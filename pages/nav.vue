<template>
  <div class="main">
    <div class="whole-nav">
      <div class="nav-menu">
        <div class="menu-close">
          <div class="line">
            <hr class="frist-line" />
            <hr class="second-line" />
          </div>
        </div>
        <div class="logo">
          <img src="../assets/image/LOGO 2.svg" alt="" />
        </div>
      </div>
      <div class="container">
        <div class="three-col">
          <div class="main-links">
            <ul class="nav-links">
              <li>
                <a href="#">Destinations</a>
              </li>
              <li>
                <a href="#">Water Park</a>
              </li>
              <li>
                <a href="#">Experiences</a>
              </li>
              <li>
                <a href="#"> SPA & Wellness</a>
              </li>
              <li><a href="#">Reservation</a></li>
              <li><a href="#">Gift Voucher</a></li>
              <li class="bottom-nav"><a href="#">Celebration & Events</a></li>
              <li><a href="#">Contact Us</a></li>
            </ul>
          </div>
          <div><hr /></div>
          <div class="second-link">
            <ul class="second-nav-links">
              <li>
                <a href="#">Bishofitu</a>
              </li>
              <li>
                <a href="#">Lake Tana </a>
              </li>
              <li>
                <a href="#">Awash</a>
              </li>
              <li>
                <a href="#">Entoto</a>
              </li>
              <li><a href="#">Semera</a></li>
            </ul>
          </div>
        </div>
        <div class="destination-links">
          <div class="dest-box">
            <div class="desti-img">
              <h3>Find Your Ideal Destination</h3>
              <img src="../assets/image/entoto.jpg" alt="" />
            </div>
            <div class="desti-desc">
              <h4>Entoto</h4>
              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Facilisis tincidunt nis
              </p>
              <div class="explore">
                <a href="#"
                  >Discover More
                  <hr
                /></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
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
  .whole-nav {
    background: #f5f5f2;
    height: 100vh;
    .nav-menu {
      display: flex;
      justify-content: space-between;
      // align-items: center;
      margin-bottom: 1rem;
      .menu-close {
        margin-top: 1rem;
        .line {
          margin-top: 1rem;
          .frist-line {
            margin: auto;

            color: $kuriftu-white;
            // height: 10rem;
            width: 2.35rem;

            -webkit-transform: rotate(45deg);
            transform: rotate(45deg);
          }
          .second-line {
            margin: auto;
            // margin-top: 1rem;
            color: $kuriftu-white;
            // height: 10rem;
            width: 2.35rem;
            -webkit-transform: rotate(-45deg);
            transform: rotate(-45deg);
          }
        }
      }
      .logo {
        margin-top: 1rem;
        width: 10rem;
        @include responsive($md) {
          width: 11rem;
        }
      }
    }
    .container {
      .three-col {
        .main-links {
          margin-top: 5rem;
          margin-bottom: 2rem;
          .nav-links {
            li {
              margin-top: 1rem;
              a {
                color: $kuriftu-grey;
                @extend .nav;
                font-size: 1.13rem;
                text-transform: uppercase;

                text-align: center;
                // font-weight: normal;
                &:hover {
                  color: $kuriftu-brown;
                }
              }
            }
            .bottom-nav {
              margin-top: 3rem;
            }
          }
        }
        .second-link {
          .second-nav-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            li {
              margin-top: 0.5rem;
              margin-bottom: 0.5rem;
              a {
                color: $kuriftu-grey;
                @extend .nav;
                font-size: 0.9rem;
                font-weight: normal;

                text-align: center;
                &:hover {
                  color: $kuriftu-brown;
                }
              }
            }
          }
        }
      }
      .destination-links {
        padding: 1rem;
        background: $kuriftu-white;

        .dest-box {
          display: flex;
          align-items: flex-end;
          .desti-img {
            img {
              width: 30rem;
            }
            h3 {
              @extend .nav;
              // margin-top: 0.94rem;
              font-size: 0.6rem;
              letter-spacing: 0.2rem;
              line-height: 0.5rem;
              margin-bottom: 0.5rem;
              color: $kuriftu-grey;
            }
          }
          .desti-desc {
            background: #fff;
            height: 10.4rem;

            h4 {
              @extend .h4;
              // margin-top: 0.94rem;
              font-size: 1rem;
              margin-left: 0.5rem;
            }
            p {
              @extend .nav;
              margin-top: 0.94rem;
              color: $kuriftu-black;
              line-height: 1rem;
              text-align: left;
              font-size: 0.7rem;
              margin-left: 0.5rem;
            }
            .explore {
              margin-top: 1.88rem;
              display: grid;
              place-items: left;
              font-size: 0.7rem;
              margin-left: 1rem;
              a {
                font-size: 0.8rem;
                color: $kuriftu-grey;
                hr {
                  color: $kuriftu-grey;
                  width: 5.5rem;
                }
              }
            }
          }
        }
      }
    }
  }
  @include responsive($md) {
    .whole-nav {
      .container {
        .three-col {
          display: flex;
          gap: 6rem;
          .main-links {
            margin-top: 5rem;
            .nav-links {
              li {
                margin-top: 2rem;
                a {
                  font-size: 1.13rem;
                  &:hover {
                    color: $kuriftu-brown;
                  }
                }
              }
              .bottom-nav {
                margin-top: 4rem;
              }
            }
          }
          div {
            hr {
              height: 25rem;
              margin-top: 7rem;
            }
          }
          .second-link {
            margin-top: 6rem;
            .second-nav-links {
              display: grid;
              gap: 0.8rem;
              li {
                margin-top: 0.5rem;
                margin-bottom: 0.5rem;
                a {
                  font-size: 1.3rem;
                }
              }
            }
          }
        }
        .destination-links {
          padding: 2rem;
          .dest-box {
            .desti-img {
              img {
                width: 20rem;
              }
              h3 {
                font-size: 0.8rem;
              }
            }
            .desti-desc {
              height: 14.3rem;
              h4 {
                margin-top: 1.94rem;
                font-size: 1.2rem;
              }
              p {
                font-size: 1rem;
                margin-top: 2rem;
              }
              .explore {
                margin-top: 2.88rem;

                font-size: 0.8rem;
                margin-left: 1rem;
                a {
                  font-size: 1rem;

                  hr {
                    width: 6.8rem;
                  }
                }
              }
            }
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .whole-nav {
      width: 90%;

      .nav-menu {
        margin-left: 2rem;
        margin-right: 2rem;
      }
      .container {
        display: flex;
        gap: 1rem;
        justify-content: center;
        .three-col {
          display: flex;
          gap: 6rem;
          .main-links {
            margin-top: 10rem;
            .nav-links {
              li {
                margin-top: 2rem;
                a {
                  font-size: 1.13rem;
                  &:hover {
                    color: $kuriftu-brown;
                  }
                }
              }
              .bottom-nav {
                margin-top: 4rem;
              }
            }
          }
          div {
            hr {
              height: 30rem;
              margin-top: 12rem;
            }
          }
          .second-link {
            margin-top: 12rem;
            margin-right: 2rem;
            .second-nav-links {
              display: grid;
              gap: 0.8rem;
              li {
                margin-top: 0.5rem;
                margin-bottom: 0.5rem;
              }
            }
          }
        }
        .destination-links {
          padding: 3rem;

          .dest-box {
            display: grid;
            margin-top: 10rem;
            .desti-img {
              img {
                width: 30rem;
              }
              h3 {
                font-size: 0.6rem;
              }
            }
            .desti-desc {
              height: 15rem;
              h4 {
                margin-top: 1.94rem;
              }
            }
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .whole-nav {
      width: 70%;
      height: 100vh;
      .nav-menu {
        margin-left: 4rem;
        margin-right: 4rem;
        margin-bottom: 3rem;
      }
      .container {
        display: flex;
        gap: 1rem;
        .three-col {
          display: flex;
          gap: 6rem;
          .main-links {
            margin-top: 7rem;
            .nav-links {
              li {
                margin-top: 2rem;
                a {
                  font-size: 1.13rem;
                  &:hover {
                    color: $kuriftu-brown;
                  }
                }
              }
              .bottom-nav {
                margin-top: 4rem;
              }
            }
          }
          div {
            hr {
              height: 30rem;
              margin-top: 9rem;
            }
          }
          .second-link {
            margin-top: 8rem;
            margin-right: 2rem;
            .second-nav-links {
              display: grid;
              gap: 0.8rem;
              li {
                margin-top: 0.5rem;
                margin-bottom: 0.5rem;
              }
            }
          }
        }
        .destination-links {
          padding: 3rem;

          .dest-box {
            display: grid;
            margin-top: 5rem;
            .desti-img {
              img {
                width: 20rem;
              }
              h3 {
                font-size: 0.6rem;
              }
            }
            .desti-desc {
              height: 11rem;
              width: 20rem;
              h4 {
                margin-top: 0.94rem;
              }
              .explore {
                margin-top: 2rem;
              }
            }
          }
        }
      }
    }
  }
  @include responsive($xxl) {
    .whole-nav {
      width: 70%;
      height: 100vh;
    }
  }
}
</style>