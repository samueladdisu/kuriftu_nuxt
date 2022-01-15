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
        <div class="destination-links">
          <ul>
            <li><a href="#">Entoto</a></li>
            <li><a href="#"></a>Waterpark</li>
            <li><a href="#"></a></li>
          </ul>
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
}
</style>