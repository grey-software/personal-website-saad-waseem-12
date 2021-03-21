<template>
  <section class="text-gray-400 body-font">
    <div class="bg-blue-900 p-4 mt-2">
      <p class="text-center">
        I love challenges and competing against the best is something that helps
        me grown even more!
      </p>
      <div class="py-2">
        <div class="grid grid-cols-1 md:grid-cols-2 mx-auto">
          <div>
            <h1 class="text-center text-2xl">Education</h1>
            <div
              v-for="edu in education"
              :key="`${edu.id}`"
              class="bg-gray-900 rounded p-4 hover:bg-blue-800 my-2 w-4/5 mx-auto"
            >
              <p class="text-xs">{{ edu.timeline }} - {{ edu.country }} <fa :icon="['fas','map-marker-alt']"/></p>
              <h1>{{ edu.program }}</h1>
              <p class="text-sm text-blue-300">{{ edu.score }}</p>
              <p class="text-sm">{{ edu.institute }}</p>
            </div>
          </div>
          <div>
            <h1 class="text-center text-2xl">Work Experience</h1>
            <div
              v-for="edu in works"
              :key="`${edu.id}`"
              class="bg-gray-900 rounded p-4 hover:bg-blue-800 my-2 w-4/5 mx-auto"
            >
              <p class="text-xs">{{ edu.timeline }} - {{ edu.country }} <fa :icon="['fas',edu.country == 'Online'? 'globe': 'map-marker-alt']"/></p>
              <h1>{{ edu.program }}</h1>
              <p class="text-sm text-blue-300">{{ edu.score }}</p>
              <p class="text-sm">{{ edu.institute }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      education: [
        {
          id: 1,
          timeline: "2017-2021",
          country: "Pakistan",
          program: "B.Sc. Computer Software Engineering",
          score: "CGPA: 3.86/4",
          institute: "University of Engineering & Technology, Mardan",
        },
        {
          id: 2,
          timeline: "2015-2017",
          country: "Pakistan",
          program: "F.Sc. Pre-Engineering",
          score: "Marks: 80%",
          institute: "Mardan Model School & College, Mardan",
        },
        {
          id: 2,
          timeline: "2013-2015",
          country: "Pakistan",
          program: "Matriculation",
          score: "Marks: 78%",
          institute: "Pakistan Learning Post School System, Abbottabad",
        },
      ],
      works: [
        {
          id: 1,
          timeline: "2018",
          country: "Pakistan",
          program: "Internet of Things Course",
          score: "",
          institute: "KP Youth Employment Program",
        },
        {
          id: 2,
          timeline: "2018-Present",
          country: "Online",
          program: "Competitive Programmer",
          score: "5 Kyu",
          institute: "Codewars",
        },
        {
          id: 3,
          timeline: "2018-2020",
          country: "Online",
          program: "Writer",
          score: "200+ Articles Published",
          institute: "Blasting News",
        },
        {
          id: 4,
          timeline: "2020",
          country: "Online",
          program: "Participant",
          score: "Placement: 8701",
          institute: "Google Code Jam",
        },
        {
          id: 5,
          timeline: "2020-Present",
          country: "Online",
          program: "Freelancer",
          score: "",
          institute: "Iconicsoft",
        },
        {
          id: 6,
          timeline: "2021-Present",
          country: "Online",
          program: "Apprentice",
          score: "",
          institute: "Grey Software",
        },
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
