<template>
  <div class="main">
    <div class="whole-nav">
      <div class="container">
        <div class="nav-menu">
          <div class="menu-close">
            <div class="line">
              <hr class="frist-line" />
              <hr class="second-line" />
            </div>
          </div>
          <div class="logo">
            <img src="../assets/image/LOGO 1.svg" alt="" />
          </div>
        </div>

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
        <hr />
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
            <li><a href="#">Semerha</a></li>
          </ul>
        </div>
      </div>
      <div class="destination-links">
        <div class="dest-box">
          <div class="desti-img">
            <h3>Featured Destination</h3>
            <img src="../assets/image/entoto.jpg" alt="" />
          </div>
          <div class="desti-desc">
            <h4>Entoto</h4>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisis
              tincidunt nis
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
    .container {
      .nav-menu {
        display: flex;
        justify-content: space-between;
        align-items: center;
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
            }
            .second-line {
              margin: auto;
              // margin-top: 1rem;
              color: $kuriftu-white;
              // height: 10rem;
              width: 2.35rem;
              -webkit-transform: rotate(-45deg);
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
      }
      .main-links {
        margin-top: 4rem;
        margin-bottom: 2rem;
        .nav-links {
          li {
            margin-top: 1rem;
            a {
              color: $kuriftu-grey;
              @extend .title;
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
            margin-top: 2rem;
          }
        }
      }
      .second-link {
        .second-nav-links {
          display: flex;
          gap: 0.8em;
          li {
            margin-top: 1rem;
            a {
              color: $kuriftu-grey;
              @extend .title;
              font-size: 0.9rem;
              font-weight: normal;

              text-align: center;
              &:hover {
                color: $kuriftu-brown;
              }
            }
          }
          .bottom-nav {
            margin-top: 2rem;
          }
        }
      }
    }
    .destination-links {
      padding: 3rem;
      // background: $kuriftu-white;
      .dest-box {
        display: flex;
        .desti-img {
          img {
            width: 20rem;
          }
        }
        .desti-desc {
          background: $kuriftu-white;

          h4 {
            @extend .h4;
            margin-top: 0.94rem;
            margin-left: 1rem;
          }
          p {
            @extend .text;
            margin-top: 0.94rem;
            color: $kuriftu-black;
            line-height: 1rem;
            text-align: left;
            margin-left: 1rem;
          }
          .explore {
            margin-top: 1.88rem;
            display: grid;
            place-items: left;
            margin-left: 1rem;
            a {
              font-size: 1rem;
              color: $kuriftu-grey;
              hr {
                color: $kuriftu-grey;
                width: 5rem;
              }
            }
          }
        }
      }
    }
  }
}
</style>