<template>
  <section>
    <div class="container">
      <div class="row p-1 align-items-center">
        <div class="col-sm-12 col-md-6  col-intro">
          <h3>Hey there!</h3>
          <h1>I'm Michael</h1>
          <h2>A junior <span>Full-Stack</span> web developer</h2>
          <button class="mt-2">
            See my works
            <span class="ms-3"
              ><img :src="require('../assets/images/work.svg')" alt=""
            /></span>
          </button>
          <button class="ms-sm-3 ms-md-0 ms-lg-4 mt-2">
            Get in contact
            <span class="ms-3"
              ><img :src="require('../assets/images/deliver.svg')" alt=""
            /></span>
          </button>
        </div>
        <div class="col-md-8 col-lg-6">
          <img :src="require('../assets/images/blob.svg')" alt="" />
        </div>
      </div>
    </div>

    <HeroLinks/>
  </section>
</template>

<script>
import HeroLinks from './HeroLinks.vue';
export default {
    name: "TheHero",
    data() {
        return {};
    },
    components: { HeroLinks }
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables";
section {
  position: relative;
  min-height: 100vh;
  background-color: #121117;
}

.container {
  padding: 150px 0 ;
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



button {
  background-color: transparent;
  color: $primary-light;
  border: 0;
  font-size: $text-small;
  border: 1px solid $primary;
  padding: 0.7rem 0.8rem;
  width: 220px;
}

@media screen and (max-width : 1200px) {
  * {
    font-size: 89%;
  }
}

@media screen and (max-width : 992px) {
  .row{
    justify-content: center;
  }
}

@media screen and (max-width : 768px) {
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
