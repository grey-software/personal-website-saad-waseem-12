<template>
  <div>
    <div class="icon-bar fixed md:ml-2">
      <a
        :href="site.link"
        v-for="site in sites"
        :key="`${site.brand}`"
        :class="[
          'block',
          'text-center',
          'p-3',
          'text-black',
          site.brand,
          'rounded-full',
          'bg-white',
          'mb-1',
          'icons',
        ]"
        target="_blank"
        ><fa :icon="['fab', site.brand]" class="text-2xl"
      /></a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sites: [
        { brand: "facebook", link: "https://www.facebook.com/darkzodiac123/" },
        { brand: "linkedin", link: "https://www.linkedin.com/in/firebelias12" },
        { brand: "github", link: "https://github.com/saad-waseem-12" },
        {
          brand: "instagram",
          link: "https://www.instagram.com/deathly_zalera/",
        },
      ],
    };
  },
};
</script>

<style scoped>
.icon-bar {
  top: 35%;
}

.icons {
  width: 48px;
  height: 48px;
}

.icon-bar a {
  transition: all 0.3s ease;
}

.facebook {
  color: #3b5998;
}

.facebook:hover {
  background-color: #3b5998;
  color: white;
}

.instagram {
  color: rgb(245, 133, 41);
}

.instagram:hover {
  background: rgb(254, 216, 119);
  background: linear-gradient(
    7deg,
    rgba(254, 216, 119, 1) 0%,
    rgba(245, 133, 41, 1) 19%,
    rgba(221, 40, 123, 1) 49%,
    rgba(129, 52, 175, 1) 74%,
    rgba(81, 91, 212, 1) 100%
  );
  color: white;
}
.google:hover {
  background: rgb(66, 133, 244);
  background: linear-gradient(
    90deg,
    rgba(66, 133, 244, 1) 0%,
    rgba(234, 67, 53, 1) 33%,
    rgba(251, 188, 5, 1) 66%,
    rgba(52, 168, 83, 1) 100%
  );
  color: white;
}

.linkedin {
  color: #0e76a8;
}

.linkedin:hover {
  background: #0e76a8;
  color: white;
}

.github {
  color: #000000;
}

.github:hover {
  background: #000000;
  color: white;
}
</style>
