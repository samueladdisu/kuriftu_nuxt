<template>
  <div class="fixed-button">
    <a class="btn btn-outline-white" href="./tana">BOOK NOW</a>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.fixed-button {
  background: $kuriftu-black;
  position: fixed;
  bottom: 0;
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
</style>