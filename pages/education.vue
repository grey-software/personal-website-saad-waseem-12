<template>
  <div>
    <Header :headline="headline" :name="name" :tags="tags" />
    <EducationHero />

  </div>
</template>

<script>
import Header from "../components/Header.vue";
import EducationHero from "../components/EducationHero.vue";

export default {
  components: {
    Header,
    EducationHero,
  },
  data() {
    return {
      headline: "My ",
      name: "Education & Experience!",
      tags: [
        "#Creative",
        "#Problem Solver",
        "#Professional",
        "#Diligent",
        "#Dreamer",
      ],
    };
  },
  head(){
    return{
      title: "Saad Waseem - Education",
    }
  }
};
</script>

<style scoped>
</style>
