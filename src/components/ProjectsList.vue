<template>
  <section class="pb-5">
    <div class="container">
      <div class="text-intro">
        <h2 class="mb-5">Projects</h2>
        <div class="row g-5 mx-auto projects-row">
          <div class="col-12 p-0" v-for="(project, i) in projects" :key="i">
            <div class="row">
              <div
                class="col-md-12 col-lg-6"
                :class="{ 'order-md-0': i % 2 === 0, 'order-md-1': i % 2 === 1 }"
              >
                <img :src="require('../assets/images/dc-comic.gif')" alt="">
              </div>
              <div class="col-6 text-light">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Dignissimos, provident?
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ProjectsList",
  data() {
    return {
      projects: [
        {
          title: "",
          description: "lorem ipsum dolor sit amet",
          image: "",
        },
        {
          title: "",
          description: "lorem ipsum dolor sit amet",
          image: "",
        },
        {
          title: "",
          description: "lorem ipsum dolor sit amet",
          image: "",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables";
section {
  background: $secondary;
}
.text-intro {
  h2 {
    text-align: center;
    color: $white;
    font-weight: bolder;
  }
}

.col-12 {
    background: #19191F;
}

img {
    aspect-ratio: 16/9;
    max-width: 100%;
}

.projects-row {
  max-width: 100%;
}

</style>
