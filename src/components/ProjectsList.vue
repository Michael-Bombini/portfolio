<template>
  <section class="py-5" id="projects">
    <div class="container">
      <div class="text-intro">
        <h2 class="mb-5">Projects</h2>
        <div class="row g-5 mx-auto projects-row">
          <div class="col-12 p-0" v-for="(project, i) in projects" :key="i">
            <div class="row">
              <div
                class="col-md-12 col-lg-6"
                :class="{
                  'order-lg-0': i % 2 === 0,
                  'order-lg-1': i % 2 === 1,
                }"
              >
                <img :src="project.image" alt="" />
              </div>
              <div class="col-md-12 col-lg-6 col-desc">
                <div class="col-desc-introduction">
                  <h2>
                    {{ project.title }}
                  </h2>
                  <p v-html="project.description"></p>
                </div>

                <a :href="project.live" class="btn-link" v-if="project.live">
                  <button>
                    Live Preview
                    <span class="ms-3"
                      ><img
                        :src="require('../assets/images/eye.svg')"
                        class="svg"
                        alt=""
                    /></span>
                  </button>
                </a>
                <a :href="project.code" class="btn-link">
                  <button
                    class="ms-sm-3 ms-md-0 ms-xl-4 mt-2"
                    :class="{ m0: !project.live }"
                  >
                    Code
                    <span class="ms-3"
                      ><img
                        :src="require('../assets/images/code.svg')"
                        class="svg"
                        alt=""
                    /></span>
                  </button>
                </a>
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
          title: "Countries Data",
          description:
            "A challenge from the frontendmentor site where i had to integrate a REST api of countries,here i've used Vue , Vue Router and Tailwind.",
          image: require("../assets/images/restcountries.png"),
          live: "https://michael-bombini-countriesdata.netlify.app/",
          code: "https://github.com/Michael-Bombini/countries-data",
        },
        {
          title: "Deliveboo",
          description:
            "My final full stack bootcamp project where together as a five member team we had to develop a complete full stack web app using all the technologies we've learned across this path. <br> This project is inspired to the famous food-delivery app Deliveroo ",
          image: require("../assets/images/deliveboo.png"),
          live: null,
          code: "https://github.com/proj-65-team4/DeliverBoo4/tree/dev",
        },
        {
          title: "Whatsapp Clone",
          description:
            "In this project i've created a whatsapp-like application where you can add fake contacts and send them messages.",
          image: require("../assets/images/whatsapp.png"),
          live: "https://michael-bombini.github.io/vue-boolzapp/",
          code: "https://github.com/Michael-Bombini/vue-boolzapp",
        },
        {
          title: "NexGen - Lead Customer",
          description:
            "In this project i've completely recreated a website using Vue Scss and Bootstrap here i've understanded better how to manage props and use the state management from the store of vue.",
          image: require("../assets/images/leadcustomer.png"),
          live: "https://michaelbombini-nexgen.netlify.app/",
          code: "https://github.com/Michael-Bombini/proj-html-vuejs",
        },
        {
          title: "DC Comics",
          description:
            "A recreation of the DC Comics site here i've learned how to manage components in a project and also created a simple image slider",
          image: require("../assets/images/dc-comic.png"),
          live: "https://michael-bombini.github.io/vue-dc-comics/",
          code: "https://github.com/Michael-Bombini/vue-dc-comics",
        },
        {
          title: "To-do List",
          description:
            "A simple To-Do list i've created using html and vue 2 from cdn.",
          image: require("../assets/images/todo.png"),
          live: "https://michael-bombini.github.io/vue-todolist/",
          code: "https://github.com/Michael-Bombini/vue-todolist",
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
  > h2 {
    color: $primary;
    text-align: center;
    font-weight: bolder;
    font-size: $heading-medium;
  }
}

.col-12 {
  background: #19191f;
}

img {
  aspect-ratio: 16/9;
  max-width: 100%;
}

.projects-row {
  max-width: 100%;
}

.col-desc {
  padding: 1.6rem;
  color: $white;
}

.col-desc-introduction {
  h2 {
    font-size: $heading-small;
    font-weight: bold;
    margin-bottom: 1.5rem;
  }

  p {
    min-width: 20ch;
    max-width: 50ch;
    line-height: 1.9rem;
    color: rgba(255, 255, 255, 0.9);
  }
}
.svg {
  width: 32px;
  height: 32px;
}
.m0 {
  margin: 0 !important;
}
img {
  object-fit: cover;
}
</style>
