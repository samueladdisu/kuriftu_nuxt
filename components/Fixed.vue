<template>
  <div class="fixed-button">
    <a class="btn btn-outline-white" @click="redirect">BOOK NOW</a>
  </div>
</template>

<script>
export default {
  methods: {
    redirect() {
      window.open(
        "https://versavvymedia.com/reservation_system/reserve.php",
        "_blank"
      );
    },
  },
};
</script>

<style lang="scss" scoped>
.fixed-button {
  background: $kuriftu-black;
  position: fixed;
  bottom: 0;
  width: 100%;
  z-index: 999;
  height: 10vh;

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
</style>