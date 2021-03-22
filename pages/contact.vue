<template>
  <div>
    <Header :headline="headline" :name="name" :tags="tags" />
    <ContactHero />

  </div>
</template>

<script>
import Header from "../components/Header.vue";
import ContactHero from "../components/ContactHero.vue";

export default {
  components: {
    Header,
    ContactHero
  },
  data() {
    return {
      headline: "",
      name: "Get In Touch!",
      tags: [
      ],
    };
  },
  head(){
    return{
      title: "Saad Waseem - Contact",
    }
  }
};
</script>

<style scoped>
</style>
