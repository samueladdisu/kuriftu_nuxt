<template>
  <div class="main">
    <HeaderApp :src="require(`../assets/image/semera.jpg`)" />

    <section class="stay-offer">
      <div class="container">
        <h2>Your Stay</h2>
        <div class="stay-offer-all">
          <div class="stay-slide" data-aos="slide-up">
            <div class="back-icon">
              <img src="../assets/image/Icons/circle-back.svg" alt="" />
            </div>
            <div class="slide-card">
              <img src="../assets/image/Bahirdar.jpg" alt="" />
            </div>
            <div class="next-icon">
              <img src="../assets/image/Icons/circle-next.svg" alt="" />
            </div>
          </div>
          <div class="stay-desc" data-aos="slide-up">
            <h4>Deluxe Suite</h4>
            <p class="header-title">
              Treat your loved ones to Ethiopia’s greatest family destination
            </p>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Facilisis
              tincidunt nisl elementum ultrices luctus habitasse. Ut orci nam
              lectus at massa enim elementum varius dictumst.
            </p>
            <div class="book-buttons">
              <a class="btn btn-primary" href="#">BUY NOW</a>
              <a class="btn btn-outline-brown" href="#">VIEW GALLERY</a>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="dining">
      <div class="container">
        <h2>Dining</h2>
        <div class="dining-wrapper">
          <div class="dining-card" data-aos="slide-up">
            <div class="dining-img">
              <img src="../assets/image/bahirdardining1.jpg" alt="" />
            </div>
            <div class="food-title">
              <h3>Desert1</h3>
            </div>
            <div class="food-desc">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            </div>
          </div>
          <div class="dining-card" data-aos="slide-up" data-aos-delay="500">
            <div class="dining-img">
              <img src="../assets/image/bahirdardining2.jpg" alt="" />
            </div>
            <div class="food-title">
              <h3>Desert2</h3>
            </div>
            <div class="food-desc">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            </div>
          </div>
          <div class="dining-card" data-aos="slide-up" data-aos-delay="600">
            <div class="dining-img">
              <img src="../assets/image/bahirdardining3.jpg" alt="" />
            </div>
            <div class="food-title">
              <h3>Desert3</h3>
            </div>
            <div class="food-desc">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="wellness">
      <div class="container">
        <h2>Wellness</h2>
      </div>
      <div class="wellness-slide">
        <div class="well-1 1">
          <img class="wellness-img" src="../assets/image/massage1.jpg" alt="" />
          <div class="image-name">
            <h5>Massages</h5>
          </div>
        </div>
        <div class="well-1 2">
          <img class="wellness-img" src="../assets/image/massage1.jpg" alt="" />
          <div class="image-name">
            <h5>Massages</h5>
          </div>
        </div>
        <div class="well-1 3">
          <img
            class="wellness-img"
            src="../assets/image/wellness-min.jpg"
            alt=""
          />
          <div class="image-name">
            <h5>Spa</h5>
          </div>
        </div>
      </div>
      <div class="container">
        <div class="wellness-button">
          <img src="../assets/image/Icons/back.svg" class="prev" alt="" />
          <img src="../assets/image/Icons/next.svg" class="next" alt="" />
        </div>
      </div>
    </section>
    <section class="event">
      <div class="container">
        <h2>Celebration and Events</h2>
        <Event />
      </div>
    </section>
    <!-- <div class="container">
      <div class="center">
        <div>
          <img src="../assets/image/event.jpg" alt="" />
        </div>
        <div>
          <img src="../assets/image/event.jpg" alt="" />
        </div>
        <div>
          <img src="../assets/image/event.jpg" alt="" />
        </div>
        <div>
          <img src="../assets/image/event.jpg" alt="" />
        </div>
        <div>
          <img src="../assets/image/event.jpg" alt="" />
        </div>
      </div>
    </div> -->
    <section class="gallery">
      <div class="container">
        <h2>Gallery</h2>
        <div class="gallery-wrapper">
          <div class="gallery-frist-img">
            <img src="../assets/image/gallery1.jpg" alt="" />
          </div>
          <div class="gallery-imgs">
            <div class="gallery-img">
              <img src="../assets/image/gallery2.jpg" alt="" />
            </div>
            <div class="gallery-img">
              <img src="../assets/image/gallery3.jpg" alt="" />
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="testimonials">
      <div class="container">
        <div class="testimony-wrapper">
          <div class="testimony-card">
            <div class="test-img">
              <img src="../assets/image/test.svg" alt="" />
            </div>
            <div class="test-stars">
              <img src="../assets/image/Icons/start.svg" alt="" />
            </div>
            <p>
              <b> Wow the best thing ever!</b> Lorem ipsum dolor sit amet,
              consectetur adipiscing elit.
            </p>
            <h3>Artist, Getachew Bezuwerk</h3>
          </div>
          <div class="testimony-card">
            <div class="test-img">
              <img src="../assets/image/test.svg" alt="" />
            </div>
            <div class="test-stars">
              <img src="../assets/image/Icons/start.svg" alt="" />
            </div>
            <p>
              <b> Wow the best thing ever!</b> Lorem ipsum dolor sit amet,
              consectetur adipiscing elit.
            </p>
            <h3>Artist, Getachew Bezuwerk</h3>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>



<script>
import AOS from "aos";
import "aos/dist/aos.css";
import Event from "../components/Event.vue";
export default {
  components: {
    Event,
  },
  data() {
    return {
      checkIn: "",
      checkOut: "",
      location: "",
      data: "",
      showNav: false,
    };
  },

  mounted() {
    AOS.init({
      duration: 1500,
      offset: 120,
      easing: "ease",
      once: false,
      anchorPlacement: "top-bottom",
    });

    gsap.registerPlugin(ScrollTrigger);

    let container = document.querySelector(".wellness");

    gsap.to(".well-1", {
      x: () =>
        -(container.scrollWidth - document.documentElement.clientWidth) + "px",

      scrollTrigger: {
        trigger: container,
        invalidateOnRefresh: true,
        // start: "top center",
        toggleActions: "restart pause reverse pause",
        pin: false,
        scrub: true,
        end: () => "+=" + container.offsetWidth,
      },
    });
  },
  methods: {
    // tabs(e) {
    //   if (e.target.classList.contains("a")) {
    //     gsap.to(".active", {
    //       duration: 1,
    //       x: 0,
    //       ease: "power3.out",
    //     });
    //     gsap.to(".event-cards", {
    //       duration: 1,
    //       x: 0,
    //       ease: "power3.out",
    //     });
    //   } else if (e.target.classList.contains("b")) {
    //     gsap.to(".active", {
    //       duration: 1,
    //       x: 100 + "%",
    //       ease: "power3.out",
    //     });
    //     gsap.to(".event-cards", {
    //       duration: 1,
    //       x: -110 + "%",
    //       ease: "power3.out",
    //     });
    //   } else if (e.target.classList.contains("c")) {
    //     gsap.to(".active", {
    //       duration: 1,
    //       x: 200 + "%",
    //       ease: "power3.out",
    //     });
    //     gsap.to(".event-cards", {
    //       duration: 1,
    //       x: -225 + "%",
    //       ease: "power3.out",
    //     });
    //   }
    // },
  },
};
</script>

<style lang="scss" scoped>
.main {
  background: $kuriftu-white;

  .stay-offer {
    margin-top: 6.25rem;
    .container {
      h2 {
        color: $kuriftu-black;
        @extend .title;
        margin-top: 0.94rem;
        text-align: left;
      }
      .stay-offer-all {
        display: flex;
        flex-direction: column;
        .stay-slide {
          margin-top: 1.88rem;
          display: flex;
          align-items: center;
          justify-items: center;
          gap: 0.5rem;
        }
        .stay-desc {
          margin-top: 1.88rem;
          margin-left: 1rem;
          margin-right: 1rem;
          h4 {
            @extend .title;
            font-size: 1.5rem;
            margin-top: 0.94rem;
            color: $kuriftu-brown;
            text-align: left;
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
            gap: 1rem;
            margin-top: 1.88rem;
          }
        }
      }
    }
  }
  @include responsive($md) {
    .stay-offer {
      .container {
        .stay-offer-all {
          .stay-slide {
            .slide-card {
              img {
                width: 25rem;
              }
            }
          }
          .stay-desc {
            // margin-left: 9rem;
            // margin-right: 9rem;

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
  @include responsive($lg) {
    .stay-offer {
      margin-top: 8.13rem;
      .container {
        .stay-offer-all {
          flex-direction: row;

          .stay-slide {
            margin-top: 4.37rem;
            .slide-card {
              img {
                width: 60rem;
              }
            }

            .next-icon,
            .back-icon {
              img {
                width: 5rem;
              }
            }
          }
          .stay-desc {
            width: 100%-20%;
            // margin-left: 5rem;
            // margin-right: 5rem;
            margin-top: 5rem;
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
    .stay-offer {
      .container {
        .stay-offer-all {
          .stay-slide {
            .slide-card {
              img {
                width: 50rem;
              }
            }
          }
        }
      }
    }
  }
  .dining {
    margin-top: 6.25rem;
    .container {
      h2 {
        color: $kuriftu-black;
        @extend .title;
        margin-top: 0.94rem;
        text-align: left;
      }
      .dining-wrapper {
        margin-top: 1.88rem;
        display: grid;
        place-items: center;

        margin-left: 2rem;
        margin-right: 2rem;
        .dining-card {
          margin-top: 1.88rem;
          .dining-img {
            position: relative;
          }
          .food-title {
            background: $kuriftu-red;
            padding: 0.8rem;
            width: 50%;
            min-width: 11.31rem;
            position: absolute;

            margin-top: -3.27rem;

            h3 {
              color: $kuriftu-white;
              @extend .caps;

              text-align: center;
            }
          }
          .food-desc {
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
          }
        }
      }
    }
  }
  @include responsive($md) {
    .dining {
      .container {
        .dining-wrapper {
          display: flex;
          gap: 1rem;
          .dining-card {
            // .dining-img {
            // }
            .food-title {
              padding: 0.5rem;
              width: 20%;
              margin-top: -2.8rem;
            }
            .food-desc {
              width: 88%;

              padding: 0.8rem;
            }
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .dining {
      margin-top: 8.13rem;
    }
  }

  @include responsive($xl) {
    .dining {
      .container {
        .dining-wrapper {
          display: flex;
          justify-content: center;
          gap: 1rem;
          .dining-card {
            .dining-img {
              width: 25rem;
            }
            .food-title {
              padding: 0.5rem;
              width: 20%;
              margin-top: -2.8rem;
            }
            .food-desc {
              width: 85%;

              padding: 1.5rem;
            }
          }
        }
      }
    }
  }
  @include responsive($xxl) {
    .dining {
      .container {
        .dining-wrapper {
          gap: 3rem;
          .dining-card {
            .food-title {
              width: 10%;
            }
            .food-desc {
              width: 80%;
            }
          }
        }
      }
    }
  }
  .event {
    margin-top: 6.25rem;
    .container {
      .tabs {
        margin: 1.88rem auto 6.25rem;
        // background: lightblue;
        display: grid;
        place-items: center;
        width: 100%;
        .tabs-container {
          display: flex;
          position: relative;
          .active {
            position: absolute;
            top: 0;
            height: 0.25rem;
            width: 5.94rem;
            transform: translate(100%, -30%);
            background: $kuriftu-black;
          }
          .tab {
            height: 0.13rem;
            width: 5.94rem;
            background: #c4c4c4;
          }
        }
      }
      h2 {
        color: $kuriftu-brown;
        @extend .title;
        margin-top: 0.94rem;
        text-align: center;
      }
    }
  }
  @include responsive($md) {
    .event {
      margin-top: 6.25rem;
      .container {
        .tabs {
          .tabs-container {
            // width: 40%;
            margin: 0 auto;
            // .tab {
            // }
          }
        }
        // .event-wrapper {
        //   gap: 6rem;
        //   .event-cards {
        //     width: 39.19rem;
        //     .event-img {
        //       width: 100%;
        //     }
        //   }
        // }
      }
    }
  }
  @include responsive($lg) {
    .event {
      margin-top: 8.13rem;
      .container {
        // .tabs {
        //   .tabs-container {
        //   }
        // }
        // .event-wrapper {
        //   width: 600%;
        // .event-cards {
        //   .event-img {
        //   }
        // }
        // }
      }
    }
  }
  .gallery {
    .container {
      h2 {
        color: $kuriftu-black;
        @extend .title;
        margin-top: 0.94rem;
      }
      .gallery-wrapper {
        .gallery-frist-img {
          margin-top: 0.94rem;
        }
        .gallery-imgs {
          .gallery-img {
            margin-top: 0.94rem;
          }
        }
      }
    }
  }
  @include responsive($md) {
    .gallery {
      .container {
        .gallery-wrapper {
          display: flex;
          justify-content: center;
          align-items: flex-start;
          gap: 1rem;
          .gallery-frist-img {
            margin-top: 1rem;
          }
          .gallery-imgs {
            .gallery-img {
              margin-top: 1rem;
            }
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .gallery {
      margin-top: 8.13rem;
      .container {
        .gallery-wrapper {
          gap: 2rem;
          margin-left: 5rem;
          margin-right: 5rem;
          margin-top: 4.37rem;
          .gallery-frist-img {
            margin-top: 2rem;
          }
          .gallery-imgs {
            .gallery-img {
              margin-top: 2rem;
            }
          }
        }
      }
    }
  }
  .destinations {
    margin-top: 6.25rem;
    .container {
      display: grid;
      place-items: center;
      h2 {
        color: $kuriftu-brown;
        @extend .title;
        margin-top: 0.94rem;
        text-align: center;
      }
      p {
        margin-top: 0.94rem;
        color: $kuriftu-grey;
        font-size: 0.88rem;
        text-align: center;
      }
      .top-2,
      .bottom-3 {
        .bishoftu,
        .bishoftu1 {
          margin-top: 1.88rem;
          .bishoftu-img {
            img {
              width: 20rem;
            }
          }
          .bishoftu-desc {
            h4 {
              @extend .h4;
              margin-top: 0.94rem;
            }
            p {
              @extend .text;
              margin-top: 0.94rem;
              color: $kuriftu-black;
              text-align: left;
            }
            .explore {
              margin-top: 1.88rem;
              display: grid;
              place-items: left;
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
  @include responsive($md) {
    .destinations {
      .container {
        .top-2 {
          display: grid;
          grid-template-columns: 1fr 1fr;
          align-items: flex-end;
          gap: 1rem;
        }
        .bottom-3 {
          display: grid;
          align-items: flex-end;
          grid-template-columns: 1fr 1fr 1fr;
          gap: 1rem;
        }
      }
    }
  }
  @include responsive($lg) {
    .destinations {
      margin-top: 8.13rem;
      .container {
        .top-2 {
          margin-top: 2.88rem;
          .bishoftu,
          .bishoftu1 {
            .bishoftu-desc {
              h4,
              p {
                margin-top: 1.88rem;
              }
            }
          }
        }
        .bottom-3 {
          margin-top: 2.88rem;
          .bishoftu {
            .bishoftu-desc {
              h4,
              p {
                margin-top: 1.88rem;
              }
            }
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .destinations {
      .container {
        .top-2 {
          margin-top: 2.88rem;
          .bishoftu,
          .bishoftu1 {
            .bishoftu-img {
              img {
                width: 40rem;
              }
            }
            .bishoftu-desc {
              h4,
              p {
                margin-top: 1.88rem;
              }
            }
          }
        }
        .bottom-3 {
          margin-top: 2.88rem;
          .bishoftu {
            .bishoftu-img {
              img {
                width: 30rem;
              }
            }
            .bishoftu-desc {
              h4,
              p {
                margin-top: 1.88rem;
              }
            }
          }
        }
      }
    }
  }
  .harmony {
    background: url(../assets/image/harmony.jpg) no-repeat;
    background-position: center center;
    background-size: cover;
    background-blend-mode: overlay;
    height: 40vh;
    // background-attachment: fixed;
    margin-top: 6.25rem;
    .container {
      position: relative;
      .harmony-text {
        // background: $kuriftu-white;
        justify-content: flex-end;
        width: 50%;
        position: absolute;
        right: 0;
        background: #fff;
        padding: 1rem;
        h4 {
          @extend .h4;

          font-size: 1.2rem;
          color: $kuriftu-brown;
          font-weight: 700;
        }
        p {
          @extend .text;
          margin-top: 0.94rem;
          color: $kuriftu-black;
          font-size: 0.88rem;
          text-align: left;
        }
        .explore {
          margin-top: 1rem;
          display: grid;
          place-items: left;
          a {
            font-size: 0.7rem;
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
  @include responsive($md) {
    .harmony {
      height: 50vh;

      .container {
        .harmony-text {
          width: 30%;
          .explore {
            a {
              font-size: 0.88rem;
            }
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .harmony {
      // background: url(../assets/image/harmony-min.jpg) no-repeat;

      margin-top: 8.13rem;
      .container {
        .harmony-text {
          h4 {
            font-size: 1.3rem;
          }
          p {
            font-size: 1rem;
          }
          width: 30%;
          .explore {
            a {
              font-size: 0.88rem;
            }
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .harmony {
      background: url(../assets/image/harmony-min.jpg) no-repeat;
      height: 70vh;
      .container {
        .harmony-text {
          h4 {
            font-size: 2rem;
            line-height: 2rem;
          }
          p {
            font-size: 1.3rem;
          }
          width: 25%;
          .explore {
            a {
              font-size: 1rem;
            }
          }
        }
      }
    }
  }
  @include responsive($xxl) {
    .harmony {
      background: url(../assets/image/harmony2.jpg) no-repeat;
      background-position: center top;
    }
  }

  .memory {
    margin-top: 6.25rem;
    .container {
      display: grid;
      place-items: center;
      h2 {
        color: $kuriftu-brown;
        @extend .title;

        margin-top: 0.94rem;
        text-align: center;
        text-transform: uppercase;
      }
      p {
        margin-top: 0.94rem;
        color: $kuriftu-grey;
        text-align: center;
      }
      .memory-slide {
        margin-top: 4.37rem;
        display: flex;
        // justify-content: space-between;
        gap: 1rem;
        .memory-slide-card {
          img {
            width: 20rem;
          }
          .img-bottom {
            background: $kuriftu-brown;

            padding: 0.5rem;
            h3 {
              color: $kuriftu-white;
              @extend .h3;
              margin-top: 0rem;
              text-align: left;
              text-transform: uppercase;
            }
            p {
              display: flex;
              margin-top: 0.94rem;
              color: $kuriftu-white;
              text-align: left;
              margin-bottom: 1rem;
              .arrow {
                width: 3rem;
              }
            }
          }
        }
      }
    }
  }
  @include responsive($md) {
    .memory {
      .container {
        .memory-slide {
          gap: 5rem;
          .memory-slide-card {
            img {
              width: 20rem;
            }
            .img-bottom {
              width: 20rem;

              p {
                .arrow {
                  width: 2rem;
                }
              }
            }
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .memory {
      margin-top: 8.13rem;
      .container {
        .memory-slide {
          gap: 8rem;
          .memory-slide-card {
            img {
              width: 25rem;
            }
            .img-bottom {
              width: 25rem;
            }
          }
        }
      }
    }
  }
  .wellness {
    margin-top: 6.25rem;
    overflow-x: hidden;
    .container {
      h2 {
        color: $kuriftu-black;
        @extend .title;

        margin-top: 0.94rem;
        text-align: left;
        // text-transform: uppercase;
      }
    }
    .wellness-slide {
      display: flex;
      margin-top: 1.88rem;
      gap: 2rem;
      margin-left: 1rem;
      width: 100vw;
      // height: 100vh;
      overflow-x: scroll;
      &::-webkit-scrollbar {
        display: none;
      }
      .well-1 {
        min-width: 100%;
        width: 100%;
        height: 100%;
        transform: translateX(0%);
        position: relative;
        .wellness-img {
          // min-height: 25.19rem;
          object-fit: cover;
        }
        .image-name {
          position: absolute;
          background: $kuriftu-brown;
          margin-top: -2.7rem;
          padding: 0.5rem 1rem;
          h5 {
            // width: 90%;
            color: $kuriftu-white;
            @extend .text;
            margin-top: 0rem;
            text-align: left;
          }
        }
      }
    }
    .container {
      .wellness-button {
        margin-top: 1.88rem;
        display: flex;
        gap: 1rem;
        transform: translateX(30%);
      }
    }
  }
  @include responsive($md) {
    .wellness {
      .wellness-slide {
        // margin-left: 13rem;

        .well-1 {
          transform: translateX(50%);
          // min-width: none;
          .image-name {
            padding-left: 2rem;
            padding-right: 2rem;
          }
        }
      }
      .container {
        .wellness-button {
          margin-top: 4.37rem;
          transform: translateX(50%);
        }
      }
    }
  }
  @include responsive($lg) {
    .wellness {
      margin-top: 8.13rem;
      .wellness-slide {
        margin-top: 4.37rem;
        .well-1 {
          transform: translateX(100%);
          min-width: auto;
          img {
            width: 100%;
          }
          .image-name {
            margin-top: -3rem;
          }
        }
      }
      .container {
        .wellness-button {
          transform: translateX(30%);
        }
      }
    }
  }
  @include responsive($xl) {
    .wellness {
      margin-top: 8.13rem;
      .wellness-slide {
        margin-top: 4.37rem;

        .well-1 {
          .image-name {
            margin-top: -3rem;
          }
        }
      }
      .container {
        .wellness-button {
          margin-top: 4.37rem;
        }
      }
    }
  }
  @include responsive($xxl) {
    .wellness {
      // .wellness-slide {
      // }
      .container {
        .wellness-button {
          gap: 3rem;
          img {
            width: 3.5rem;
          }
        }
      }
    }
  }

  .testimonials {
    margin-top: 6.25rem;
    .container {
      .testimony-wrapper {
        display: flex;
        justify-content: center;
        gap: 2rem;
        .testimony-card {
          background: #fff;
          padding: 1rem;
          border-radius: 0.5rem;
          width: 20rem;
          .test-img {
            margin-top: -3rem;
            margin-left: -1.5rem;
            img {
              width: 4rem;
            }
          }
          .test-stars {
            img {
              margin-left: 1rem;
              width: 10rem;
            }
          }
          p {
            margin-left: 1rem;
            color: $kuriftu-black;
            @extend .title;
            font-family: "Neue Helvetica Light Italic";
            font-size: 0.88rem;
            margin-top: 0.98rem;
            line-height: 1.3rem;
            text-align: left;
          }
          h3 {
            margin-left: 1rem;
            color: $kuriftu-red;
            @extend .h3;
            font-family: "Neue Helvetica Extended Bold";
            font-size: 0.8rem;
            margin-top: 0.98rem;
            line-height: 1.3rem;
            text-align: left;
          }
        }
      }
    }
  }
}
</style>