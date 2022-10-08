<template>
  <section class="py-5">
    <div class="container">
      <div class="row g-5">
        <div class="col-12 mb-5 col-md-6">
          <h2><strong>About Me</strong> & <strong>Tech</strong></h2>
          <p class="mt-4">
            Since I was a child I have always been passionate about technology,
            with time I discovered the world of programming where I felt free
            to unleash my <strong>Creativity</strong> this passion today continues to be
            stimulated by <strong>Discovering</strong> and keep <strong>Learning</strong> and new things.
          </p>
        </div>
        <div class="col-12 col-md-6">
          <img :src="require('../assets/images/techstack.png')" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables";
section {
  background: $secondary;
}
h2 {
  max-width: 8ch;
  font-size: clamp(2rem , 7vw , $heading-medium);
  color: $white;
}
img {
  min-width: 300px;
  max-width: 100%;
}
p {
  max-width: 550px;
  color: rgba(255, 255, 255, 0.9);
  line-height: 185%;
}
strong {
  color: $primary-light;
}



</style>
