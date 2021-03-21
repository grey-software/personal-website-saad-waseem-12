<template>
  <section class="text-gray-400 body-font">
    <div class="bg-blue-900 p-4 mt-2">
      <p class="text-center">
        I like to experiment with different technologies and create different
        kinds of applications!
      </p>
      <h1 class="text-center sm:text-4xl text-3xl">My Skills!</h1>
      <div class="grid grid-cols-3 md:grid-cols-4 w-5/6 md:w-3/5 mx-auto">
        <div
          class="text-center mt-2"
          v-for="skill in skills"
          :key="`${skill.name}`"
        >
          <fa
            v-if="skill.icon != null"
            :icon="[skill.icontype, skill.icon]"
            class="skill-icon"
          /><img
            v-if="skill.img != null"
            :src="getImgUrl(skill.img)"
            class="h-20 mx-auto"
          />
          <p class="mt-3">{{ skill.name }}</p>
        </div>
      </div>
    </div>
    <div class="container px-5 mx-auto w-5/6 py-4">
      <h1 class="text-center sm:text-4xl text-3xl mb-4">My Projects!</h1>
      <div
        class="flex items-center lg:w-3/5 mx-auto border-b pb-10 mb-10 border-gray-800 sm:flex-row flex-col"
      >
        <div
          class="sm:w-32 sm:h-32 h-20 w-20 sm:mr-10 inline-flex items-center justify-center rounded-full text-pink-400 bg-gray-800 flex-shrink-0"
        >
          <fa :icon="['fas','mobile-alt']" class="text-4xl md:text-6xl"/>
        </div>
        <div class="flex-grow sm:text-left text-center mt-6 sm:mt-0">
          <h2 class="text-white text-lg title-font font-medium mb-2">
            Omega Fortnite Challenge Guide
          </h2>
          <p class="leading-relaxed text-base">
            An Android Application that helps Fortnite players to easily complete challenges, check daily item shop, test their network latency, and find other players to team up with.
          </p>
          <a target="_blank" href="https://play.google.com/store/apps/details?id=com.infernalbits.omega_fortnitechallengeguide&hl=en&gl=US" class="mt-3 text-pink-400 inline-flex items-center"
            >Learn More
            <svg
              fill="none"
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              class="w-4 h-4 ml-2"
              viewBox="0 0 24 24"
            >
              <path d="M5 12h14M12 5l7 7-7 7"></path>
            </svg>
          </a>
        </div>
      </div>
      <div
        class="flex items-center lg:w-3/5 mx-auto border-b pb-10 mb-10 border-gray-800 sm:flex-row flex-col"
      >
        <div class="flex-grow sm:text-left text-center mt-6 sm:mt-0">
          <h2 class="text-white text-lg title-font font-medium mb-2">
            Diet Planner
          </h2>
          <p class="leading-relaxed text-base">
            A web application for creating a meal plan that would help users reach their target weight goal in specified duration.
          </p>
        </div>
        <div
          class="sm:w-32 order-first sm:order-none sm:h-32 h-20 w-20 sm:ml-10 inline-flex items-center justify-center rounded-full text-pink-400 bg-gray-800 flex-shrink-0"
        >
          <fa :icon="['fas','utensils']" class="text-4xl md:text-6xl"/>
        </div>
      </div>
      <div class="flex items-center lg:w-3/5 mx-auto sm:flex-row flex-col">
        <div
          class="sm:w-32 sm:h-32 h-20 w-20 sm:mr-10 inline-flex items-center justify-center rounded-full text-pink-400 bg-gray-800 flex-shrink-0"
        >
          <fa :icon="['fas','images']" class="text-4xl md:text-6xl"/>
        </div>
        <div class="flex-grow sm:text-left text-center mt-6 sm:mt-0">
          <h2 class="text-white text-lg title-font font-medium mb-2">
            Cloud Image Processor
          </h2>
          <p class="leading-relaxed text-base">
            A cloud based image processor that can fetch image and process it to create a social media post and upload it to Imgur.
          </p>

        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        { name: "Java", icon: "java", icontype: "fab" },
        { name: "Android", icon: "android", icontype: "fab" },
        { name: "HTML 5", icon: "html5", icontype: "fab" },
        { name: "CSS 3", icon: "css3", icontype: "fab" },
        { name: "Firebase", img: "firebase" },
        { name: "Kotlin", img: "kotlin" },
        { name: "C/C++", img: "c++" },
        { name: "Javascript", icon: "js", icontype: "fab" },
        { name: "NodeJS", icon: "node", icontype: "fab" },
        { name: "Python", icon: "python", icontype: "fab" },
        { name: "Content Writer", icon: "pen", icontype: "fas" },
        { name: "Pro Gamer", icon: "gamepad", icontype: "fas" },
      ],
    };
  },

  methods: {
    getImgUrl(pic) {
      var images = require.context("../assets/icons/", false, /\.svg$/);
      return images("./" + pic + ".svg");
    },
  },
};
</script>

<style scoped>
p {
  font-family: "Poppins", sans-serif;
}

h1 {
  font-family: "Poppins", sans-serif;
  font-weight: 600;
}

.skill-icon {
  font-size: 5rem;
}
</style>
