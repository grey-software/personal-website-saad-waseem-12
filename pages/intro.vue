<template>
  <div>
    <Header :name="name" :tags="tags" />
    <Hero />

  </div>
</template>

<script>
import Header from "../components/Header.vue";
import Hero from "../components/Hero.vue";

export default {
  components: {
    Header,
    Hero,
  },
  data() {
    return {
      name: "Saad",
      tags: [
        "#Software Engineer",
        "#Developer",
        "#Explorer",
        "#Gamer",
        "#Weeb",
      ],
    };
  },
};
</script>

<style scoped>
</style>
