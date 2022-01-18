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

    <section class="story">
      <div class="container">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisis
          tincidunt nisl elementum ultrices luctus habitasse. Ut orci nam lectus
          at massa enim elementum varius dictumst. Nulla a, sed enim turpis non
          lacinia fusce. Quis volutpat sit ullamcorper vitae magna vel sit
          pharetra scelerisque.
        </p>
      </div>
    </section>
    <section class="story-picture">
      <div class="container">
        <div class="story-wrapper">
          <div class="story-card">
            <img src="../assets/image/friststory.jpg" alt="" />

            <div class="back-card"></div>
          </div>
          <div class="story-card1">
            <h2>How It All Began</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisis
              tincidunt nisl elementum ultrices luctus habitasse. Ut orci nam
              lectus at massa enim elementum varius dictumst. Nulla a, sed enim
              turpis non lacinia fusce. Quis volutpat sit ullamcorper vitae
              magna vel sit pharetra scelerisque.
            </p>
          </div>
        </div>
        <div class="story-wrapper">
          <div class="story-card reverse">
            <img src="../assets/image/secondstory.jpg" alt="" />

            <div class="back-card"></div>
          </div>
          <div class="story-card1 reverse1">
            <h2>The Past Years</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisis
              tincidunt nisl elementum ultrices luctus habitasse. Ut orci nam
              lectus at massa enim elementum varius dictumst. Nulla a, sed enim
              turpis non lacinia fusce. Quis volutpat sit ullamcorper vitae
              magna vel sit pharetra scelerisque.
            </p>
          </div>
        </div>
        <div class="story-wrapper">
          <div class="story-card">
            <img src="../assets/image/thridstory.jpg" alt="" />

            <div class="back-card"></div>
          </div>
          <div class="story-card1">
            <h2>The Persent</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisis
              tincidunt nisl elementum ultrices luctus habitasse. Ut orci nam
              lectus at massa enim elementum varius dictumst. Nulla a, sed enim
              turpis non lacinia fusce. Quis volutpat sit ullamcorper vitae
              magna vel sit pharetra scelerisque.
            </p>
          </div>
        </div>
      </div>
    </section>
    <section class="special-offer">
      <div class="container">
        <h2>Explore Our Packages</h2>
        <div class="special-offer-all" style="overflow-x: hidden">
          <div class="special-slide" data-aos="slide-right">
            <div class="back-icon">
              <img src="../assets/image/Icons/circle-back.svg" alt="" />
            </div>
            <div class="slide-card">
              <img src="../assets/image/storyoffer.jpg" alt="" />
            </div>
            <div class="next-icon">
              <img src="../assets/image/Icons/circle-next.svg" alt="" />
            </div>
          </div>
          <div class="gift-desc" data-aos="slide-left">
            <h3>special offer</h3>
            <h4>Gift Vouchers</h4>
            <p class="header-title">
              Treat your loved ones to Ethiopia’s greatest family destination
            </p>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisis
              tincidunt nisl elementum ultrices luctus habitasse. Ut orci nam
              lectus at massa enim elementum varius dictumst. Nulla a, sed enim
              turpis non lacinia fusce. Quis volutpat sit ullamcorper vitae
              magna vel sit pharetra scelerisque.
            </p>
            <div class="book-buttons">
              <a class="btn btn-outline-black" href="#">GET OFFERS</a>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.main {
  header {
    background: url("../assets/image/ourstory.jpg") rgba(0, 6, 27, 0.22)
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

  .story {
    margin-top: 6.25rem;
    .container {
      p {
        @extend .text;
        margin-top: 0.94rem;
        color: $kuriftu-grey;
        font-weight: 400;
        font-size: 1rem;
        text-align: center;
      }
    }
  }
  @include responsive($lg) {
    .story {
      margin-top: 8.13rem;
      margin-left: 3rem;
      margin-right: 3rem;
    }
  }
  @include responsive($xl) {
    .story {
      margin-left: 10rem;
      margin-right: 10rem;
    }
  }
  .story-picture {
    margin-top: 6.25rem;
    .container {
      .story-wrapper {
        margin-top: 2.88rem;
        .story-card {
          display: grid;
          position: relative;

          img {
            width: 18rem;
          }
          .back-card {
            position: absolute;
            background: #fff;
            z-index: -1;
            top: 1.69rem;
            left: 1.69rem;
            width: 18rem;
            height: 13rem;
          }
        }
        .story-card1 {
          // margin-top: 16rem;
          h2 {
            color: $kuriftu-brown;
            @extend .title;
            margin-top: 3rem;
            margin-bottom: 2rem;
            font-weight: 200;
            text-align: left;
          }
          p {
            @extend .text;
            margin-top: 0.94rem;
            color: $kuriftu-black;
            font-size: 0.9rem;
            text-align: left;
          }
        }
      }
    }
  }
  @include responsive($md) {
    .story-picture {
      .container {
        .story-wrapper {
          display: grid;
          grid-template-columns: 1fr 1fr;
          // align-items: center;
          gap: 3rem;
          .reverse {
            grid-column-start: 2;
          }
          .reverse1 {
            grid-column-start: 1;
            grid-row-start: 1;
          }
          .story-card1 {
            margin-top: 6rem;
          }
        }
      }
    }
  }

  @include responsive($lg) {
    .story-picture {
      margin-top: 8.13rem;
      .container {
        .story-wrapper {
          margin-top: 4.37rem;
          // place-items: center;
          .story-card {
            img {
              width: 20rem;
            }

            .back-card {
              z-index: -1;
              top: 1.69rem;
              left: 1.69rem;
              width: 20.38rem;
              height: 14.94rem;
            }
          }
          .story-card1 {
            margin-top: 8rem;
            h2 {
              margin-top: 0rem;
              width: 12rem;
              line-height: 2.5rem;
            }
          }
        }
      }
    }
  }

  @include responsive($xl) {
    .story-picture {
      margin-top: 8.13rem;
      .container {
        width: 100%-20%;
        .story-wrapper {
          place-items: center;
          gap: 0rem;
          margin-top: 5rem;
          .story-card {
            img {
              width: 28rem;
            }

            .back-card {
              z-index: -1;
              top: 2.69rem;
              left: 2.69rem;
              width: 27.38rem;
              height: 19.94rem;
            }
          }
          .story-card1 {
            p {
              width: 30rem;
            }
          }
        }
      }
    }
  }
  .special-offer {
    margin-top: 6.25rem;
    .container {
      h2 {
        color: $kuriftu-black;
        @extend .title;
        margin-top: 0.94rem;
        margin-bottom: 2rem;
        text-align: left;
      }
      .special-offer-all {
        display: grid;
        place-items: center;
        // margin: 0 auto;
        // width: 20rem;
        .special-slide {
          display: flex;
          align-items: center;
          justify-items: center;
          gap: 0.5rem;
          .back-icon,
          .next-icon {
            img {
              width: 2rem;
            }
          }
        }
        .gift-desc {
          margin-top: 1.88rem;
          margin-left: 1rem;
          margin: 0 auto;
          width: 20rem;
          h3 {
            @extend .nav;
            margin-top: 0.94rem;
            font-size: 0.7rem;
            letter-spacing: 0.2rem;
            line-height: 0.5rem;
            margin-bottom: 0.5rem;
            font-weight: 600;
            text-transform: uppercase;
            color: $kuriftu-grey;
          }
          h4 {
            @extend .title;
            margin-top: 1.88rem;
            color: $kuriftu-black;
          }
          .header-title {
            color: $kuriftu-grey;
          }
          p {
            @extend .text;
            margin-top: 0.94rem;
            color: $kuriftu-black;
            font-size: 0.88rem;
            text-align: left;
          }
          .book-buttons {
            display: flex;
            justify-content: left;

            margin-top: 1.88rem;
          }
        }
      }
    }
  }
  @include responsive($md) {
    .special-offer {
      // width: 100%;
      .container {
        .special-offer-all {
          .special-slide {
            .slide-card {
              img {
                width: 25rem;
              }
            }
          }
          .gift-desc {
            width: 25rem;
            // margin-left: 5rem;
            // margin-right: 5rem;
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .special-offer {
      margin-top: 8.13rem;
      .container {
        .special-offer-all {
          display: flex;

          .special-slide {
            .slide-card {
              img {
                width: 25rem;
              }
            }

            .next-icon,
            .back-icon {
              img {
                width: 2rem;
              }
            }
          }
          .gift-desc {
            margin-left: 1rem;
            margin-right: 1rem;
            margin: 0 auto;
            width: 25rem;
            .book-buttons {
              display: flex;
              justify-content: left;

              margin-top: 1.88rem;
            }
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .special-offer {
      .container {
        .special-offer-all {
          display: flex;
          align-items: flex-start;
          margin-top: 4.37rem;
          .special-slide {
            .slide-card {
              img {
                width: 30rem;
              }
            }
          }
          .gift-desc {
            margin-left: 2rem;
            margin-right: 2rem;
            width: 30rem;
          }
        }
      }
    }
  }
}
</style>