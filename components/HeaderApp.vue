<template>
  <div>
    <transition
      appear
      @before-enter="beforeEnter"
      @enter="enter"
      @before-leave="beforeLeave"
      @leave="leave"
      @after-leave="afterLeave"
    >
      <NavMenu v-if="showNav" @close="closeNav" />
    </transition>
    <header>
      <img :src="src" class="bg-img" alt="" />
      <div class="bg-linear"></div>
      <nav>
        <div class="container top-nav">
          <div class="menu-line" @click="toggleNav">
            <div class="line">
              <hr />
              <hr />
            </div>
          </div>
          <div class="logo">
            <nuxt-link to="/">
              <img src="../assets/image/LOGO 1.svg" alt="" />
            </nuxt-link>
          </div>

          <div class="nav-book-button">
            <a class="btn btn-outline-white" @click="redirect">BOOK NOW</a>
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
  </div>
</template>

<script>
import NavMenu from "../components/NavMenu.vue";

export default {
  props: ["src"],
  components: {
    NavMenu,
  },
  data() {
    return {
      showNav: false,
    };
  },
  methods: {
    toggleNav() {
      this.showNav = !this.showNav;
    },
    redirect() {
      window.open(
        "https://versavvymedia.com/reservation_system/reserve.php",
        "_blank"
      );
    },
    closeNav() {
      this.showNav = !this.showNav;
    },
    beforeEnter(el) {
      console.log("before enter ");
      el.style.transform = "translateX(-100%)";
    },

    enter(el, done) {
      console.log("starting to enter");
      gsap.to(el, {
        duration: 1,
        x: 0,
        ease: "circ.out",
        onComplete: done,
      });
    },
    beforeLeave(el) {
      console.log("before leave ");
      el.style.transform = "translateX(0)";
    },

    leave(el, done) {
      console.log("starting to leave");
      gsap.to(el, {
        duration: 1,
        x: -100 + "%",
        ease: "expo.out",
        onComplete: done,
      });
    },
    afterLeave() {
      console.log("after leave");
    },
  },
};
</script>

<style lang="scss" scoped>
header {
  width: 100%;
  height: 100vh;
  position: relative;
  &::after {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgb(0, 6, 27);
  }
  .bg-img {
    z-index: 1;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .bg-linear {
    background: linear-gradient(180deg, #000000 -35.31%, rgba(0, 0, 0, 0) 100%);
    width: 100%;
    height: 20vh;
    position: absolute;
    top: 0;
  }
  nav {
    z-index: 999;
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    .top-nav {
      position: sticky;
      top: 0;
      bottom: 0;
      width: 90%;
      margin: 0 auto;
    }
    .container {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      .menu-line {
        margin-top: 1rem;
        cursor: pointer;
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