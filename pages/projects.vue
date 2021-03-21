<template>
  <div>
    <Header :headline="headline" :name="name" :tags="tags" />
    <ProjectHero />

  </div>
</template>

<script>
import Header from "../components/Header.vue";
import ProjectHero from "../components/ProjectHero.vue";

export default {
  components: {
    Header,
    ProjectHero,
  },
  data() {
    return {
      headline: "Things I've ",
      name: "Worked On!",
      tags: [
        "#Android Applications",
        "#Desktop Applications",
        "#Websites",
        "#Cloud Processing",
        "#Articles",
      ],
    };
  },
};
</script>

<style scoped>
</style>
