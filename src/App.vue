<template>
  <div id="app">
    <TheHero />
    <h1 class="bg-danger text-center fw-bold">WORK IN PROGRESS!</h1>
  </div>
</template>

<script>
import TheHero from "./components/TheHero.vue";

export default {
  name: "App",
  components: {
    TheHero,
  },
};
</script>

<style lang="scss">
@import "assets/styles/main.scss";


// html ,body {
//   overflow-x: hidden;
// }


</style>
