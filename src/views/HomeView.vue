<template>
  <main ref="container" data-scroll-container>
    <section class="home-section">
      <homepage></homepage>
    </section>

    <section class="about-section">
      <aboutshort></aboutshort>
    </section>

    <!-- <section class="services-section">
      <servicespage></servicespage>
    </section> -->

    <section class="services-section">
      <projectspage></projectspage>
    </section>

    <section class="aboutmore-section">
      <aboutmore></aboutmore>
    </section>


    <footer>

      <p>©2023 | Urazaliyev Ikrombek</p>

    </footer>

  </main>
</template>

<script>
import homepage from "@/components/homepage.vue"
import aboutshort from "@/components/aboutshort.vue"
import servicespage from "@/components/servicespage.vue"
import projectspage from "@/components/projectspage.vue"
import aboutmore from "@/components/aboutmore.vue"

export default {
  components: {
    homepage,
    aboutshort,
    servicespage,
    projectspage,
    aboutmore,
  },
}

</script>




<style lang="scss" scoped>
footer {
  margin-top: 10rem;
  padding: 1.4rem;
  border-top: 1px solid #ffffff4f;
  text-align: center;
  font-size: 1rem;
  color: #fff;
}
</style>