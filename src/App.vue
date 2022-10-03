<template>
  <div id="app">
    <TheHero />
    <AboutTech/>
    <ProjectsList/>
  </div>
</template>

<script>
import TheHero from "./components/TheHero.vue";
import ProjectsList from "./components/ProjectsList.vue";
import AboutTech from "./components/AboutTech.vue";

export default {
  name: "App",
  components: {
    TheHero,
    ProjectsList,
    AboutTech
},
};
</script>

<style lang="scss">
@import "assets/styles/main.scss";

html , body {
  overflow-x: hidden ;
}



</style>
