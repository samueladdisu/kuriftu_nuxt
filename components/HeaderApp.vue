<template>
  <header>
    <!-- <img src="~/assets/image/Home.jpg" class="header-img" alt=""> -->
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
</template>

<script>
export default {

}
</script>

<style lang="scss">
 header {
    background: url("~/assets/image/Home.jpg") no-repeat;
    background-position: center center;
    background-size: cover;
    background-blend-mode: overlay;
    width: 100%;
    height: 90vh;
    // z-index: -1;
    // position: relative;
    .header-img{
      position: absolute;
      top: 0;
      z-index: -1;
    }
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
</style>