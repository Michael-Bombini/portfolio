<template>
  <section>
    <div class="container">
      <div class="row p-1 align-items-center">
        <div class="col-sm-12 col-md-6 col-intro">
          <h3>Hey there!</h3>
          <h1>I'm Michael</h1>
          <h2>A junior <span>Full-Stack</span> web developer</h2>
          <a href="" class="btn-link">
            <button class="mt-2">
              See my works
              <span class="ms-3"
                ><img :src="require('../assets/images/work.svg')" alt=""
              /></span>
            </button>
          </a>
          <a href="" class="btn-link">
            <button class="ms-sm-3 ms-md-0 ms-lg-4 mt-2">
              Get in contact
              <span class="ms-3"
                ><img :src="require('../assets/images/deliver.svg')" alt=""
              /></span>
            </button>
          </a>
        </div>
        <div class="col-md-8 col-lg-6 col-image">
          <img :src="require('../assets/images/michael.png')" alt="" />
        </div>
      </div>
    </div>

    <HeroLinks />
  </section>
</template>

<script>
import gsap from "gsap";
import HeroLinks from "./HeroLinks.vue";

export default {
  name: "TheHero",
  components: { HeroLinks },
  data() {
    return {};
  },
  methods: {},

  mounted() {
    gsap.fromTo(
      ".col-intro",
      { y: -120, opacity: 0 },
      { y: 0, opacity: 1, duration: 0.8 }
    );
    gsap.fromTo(
      ".col-image",
      { y: 100, opacity: 0 },
      { y: 0, opacity: 1, duration: 0.6, delay: 0.7 }
    );
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables";
section {
  position: relative;
  min-height: 100vh;
  background-color: $secondary;
}

.container {
  padding: 90px 0;
}

img {
  max-width: 100%;
}

h1 {
  font-size: $heading-big;
  font-weight: 700;
  color: $primary;
}

h2 {
  width: 20ch;
  font-size: $heading-medium;
  font-weight: 700;
  color: $white;
  margin-bottom: 2.8rem;
}

span {
  color: $primary;
}

h3 {
  font-size: $heading-small;
  font-weight: 600;
  color: $white;
  margin-bottom: 1.5rem;
  position: relative;
}

h3::before {
  content: "";
  display: block;
  width: 3px;
  height: 42px;
  background: $primary;
  position: absolute;
  bottom: 0;
  left: -5%;
}

@media screen and (max-width: 1200px) {
  * {
    font-size: 89%;
  }
}

@media screen and (max-width: 992px) {
  .row {
    justify-content: center;
  }
}

@media screen and (max-width: 768px) {
  .row {
    max-width: 100%;
  }
  * {
    font-size: 83%;
  }
  .col-intro {
    text-align: center;
  }
  h2 {
    margin: auto;
    margin-bottom: 1.8rem;
  }
}
</style>
