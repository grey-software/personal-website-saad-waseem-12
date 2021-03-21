<template>
  <div class="grid md:grid-cols-1 text-center">
    <h2 class="text-white">
      {{headline}}<span class="name text-white ml-2">{{ name }}</span>
    </h2>
    <div
      class="mt-5 flex flex-wrap w-4/5 justify-center md:w-2/5 ml-auto mr-auto"
    >
      <p
        class="rounded-xl text-base m-1 tagged inline text-white p-2 bg-black cursor-default"
        v-for="tag in tags"
        :key="`${tag}`"
      >
        {{ tag }}
      </p>
    </div>
    <!-- <div class="grid md:justify-items-start justify-items-center"><img src="../assets/images/fb.png" class="w-10"></div> -->
  </div>
</template>

<script>
export default {
  props: {
    headline: String,
    name: String,
    tags: Array,
  },
};
</script>

<style scoped>
span {
  font-size: 7vh;
  font-family: "Pacifico", cursive;
}

h2 {
  font-size: 5.7vh;
  font-family: "Pacifico", cursive;
}

.name {
  animation: animated-rainbow-shadow 1s infinite;
}

.tagged {
  background: rgb(54, 116, 173);
  background: linear-gradient(
    87deg,
    rgba(54, 116, 173, 1) 0%,
    rgba(54, 96, 173, 1) 100%
  );
}

@keyframes animated-rainbow-shadow {
  0% {
    text-shadow: 0px 0px transparent, 1px 1px red, 2px 2px red, 3px 3px red,
      4px 4px red, 5px 5px red, 6px 6px red, 7px 7px orange, 8px 8px orange,
      9px 9px orange, 10px 10px orange, 11px 11px orange, 12px 12px orange,
      13px 13px yellow, 14px 14px yellow, 15px 15px yellow, 16px 16px yellow,
      17px 17px yellow, 18px 18px yellow, 19px 19px blue, 20px 20px blue,
      21px 21px blue, 22px 22px blue, 23px 23px blue, 24px 24px blue,
      25px 25px red;
  }
  4% {
    text-shadow: 0px 0px transparent, 1px 1px red, 2px 2px red, 3px 3px red,
      4px 4px red, 5px 5px red, 6px 6px orange, 7px 7px orange, 8px 8px orange,
      9px 9px orange, 10px 10px orange, 11px 11px orange, 12px 12px yellow,
      13px 13px yellow, 14px 14px yellow, 15px 15px yellow, 16px 16px yellow,
      17px 17px yellow, 18px 18px blue, 19px 19px blue, 20px 20px blue,
      21px 21px blue, 22px 22px blue, 23px 23px blue, 24px 24px red,
      25px 25px red;
  }
  8% {
    text-shadow: 0px 0px transparent, 1px 1px red, 2px 2px red, 3px 3px red,
      4px 4px red, 5px 5px orange, 6px 6px orange, 7px 7px orange,
      8px 8px orange, 9px 9px orange, 10px 10px orange, 11px 11px yellow,
      12px 12px yellow, 13px 13px yellow, 14px 14px yellow, 15px 15px yellow,
      16px 16px yellow, 17px 17px blue, 18px 18px blue, 19px 19px blue,
      20px 20px blue, 21px 21px blue, 22px 22px blue, 23px 23px red,
      24px 24px red, 25px 25px red;
  }
  12% {
    text-shadow: 0px 0px transparent, 1px 1px red, 2px 2px red, 3px 3px red,
      4px 4px orange, 5px 5px orange, 6px 6px orange, 7px 7px orange,
      8px 8px orange, 9px 9px orange, 10px 10px yellow, 11px 11px yellow,
      12px 12px yellow, 13px 13px yellow, 14px 14px yellow, 15px 15px yellow,
      16px 16px blue, 17px 17px blue, 18px 18px blue, 19px 19px blue,
      20px 20px blue, 21px 21px blue, 22px 22px red, 23px 23px red,
      24px 24px red, 25px 25px red;
  }
  16% {
    text-shadow: 0px 0px transparent, 1px 1px red, 2px 2px red, 3px 3px orange,
      4px 4px orange, 5px 5px orange, 6px 6px orange, 7px 7px orange,
      8px 8px orange, 9px 9px yellow, 10px 10px yellow, 11px 11px yellow,
      12px 12px yellow, 13px 13px yellow, 14px 14px yellow, 15px 15px blue,
      16px 16px blue, 17px 17px blue, 18px 18px blue, 19px 19px blue,
      20px 20px blue, 21px 21px red, 22px 22px red, 23px 23px red, 24px 24px red,
      25px 25px red;
  }
  20% {
    text-shadow: 0px 0px transparent, 1px 1px red, 2px 2px orange,
      3px 3px orange, 4px 4px orange, 5px 5px orange, 6px 6px orange,
      7px 7px orange, 8px 8px yellow, 9px 9px yellow, 10px 10px yellow,
      11px 11px yellow, 12px 12px yellow, 13px 13px yellow, 14px 14px blue,
      15px 15px blue, 16px 16px blue, 17px 17px blue, 18px 18px blue,
      19px 19px blue, 20px 20px red, 21px 21px red, 22px 22px red, 23px 23px red,
      24px 24px red, 25px 25px red;
  }
  24% {
    text-shadow: 0px 0px transparent, 1px 1px orange, 2px 2px orange,
      3px 3px orange, 4px 4px orange, 5px 5px orange, 6px 6px orange,
      7px 7px yellow, 8px 8px yellow, 9px 9px yellow, 10px 10px yellow,
      11px 11px yellow, 12px 12px yellow, 13px 13px blue, 14px 14px blue,
      15px 15px blue, 16px 16px blue, 17px 17px blue, 18px 18px blue,
      19px 19px red, 20px 20px red, 21px 21px red, 22px 22px red, 23px 23px red,
      24px 24px red, 25px 25px red;
  }
  28% {
    text-shadow: 0px 0px transparent, 1px 1px orange, 2px 2px orange,
      3px 3px orange, 4px 4px orange, 5px 5px orange, 6px 6px yellow,
      7px 7px yellow, 8px 8px yellow, 9px 9px yellow, 10px 10px yellow,
      11px 11px yellow, 12px 12px blue, 13px 13px blue, 14px 14px blue,
      15px 15px blue, 16px 16px blue, 17px 17px blue, 18px 18px red,
      19px 19px red, 20px 20px red, 21px 21px red, 22px 22px red, 23px 23px red,
      24px 24px red, 25px 25px orange;
  }
  32% {
    text-shadow: 0px 0px transparent, 1px 1px orange, 2px 2px orange,
      3px 3px orange, 4px 4px orange, 5px 5px yellow, 6px 6px yellow,
      7px 7px yellow, 8px 8px yellow, 9px 9px yellow, 10px 10px yellow,
      11px 11px blue, 12px 12px blue, 13px 13px blue, 14px 14px blue,
      15px 15px blue, 16px 16px blue, 17px 17px red, 18px 18px red,
      19px 19px red, 20px 20px red, 21px 21px red, 22px 22px red, 23px 23px red,
      24px 24px orange, 25px 25px orange;
  }
  36% {
    text-shadow: 0px 0px transparent, 1px 1px orange, 2px 2px orange,
      3px 3px orange, 4px 4px yellow, 5px 5px yellow, 6px 6px yellow,
      7px 7px yellow, 8px 8px yellow, 9px 9px yellow, 10px 10px blue,
      11px 11px blue, 12px 12px blue, 13px 13px blue, 14px 14px blue,
      15px 15px blue, 16px 16px red, 17px 17px red, 18px 18px red, 19px 19px red,
      20px 20px red, 21px 21px red, 22px 22px red, 23px 23px orange,
      24px 24px orange, 25px 25px orange;
  }
  40% {
    text-shadow: 0px 0px transparent, 1px 1px orange, 2px 2px orange,
      3px 3px yellow, 4px 4px yellow, 5px 5px yellow, 6px 6px yellow,
      7px 7px yellow, 8px 8px yellow, 9px 9px blue, 10px 10px blue,
      11px 11px blue, 12px 12px blue, 13px 13px blue, 14px 14px blue,
      15px 15px red, 16px 16px red, 17px 17px red, 18px 18px red, 19px 19px red,
      20px 20px red, 21px 21px red, 22px 22px orange, 23px 23px orange,
      24px 24px orange, 25px 25px orange;
  }
  44% {
    text-shadow: 0px 0px transparent, 1px 1px orange, 2px 2px yellow,
      3px 3px yellow, 4px 4px yellow, 5px 5px yellow, 6px 6px yellow,
      7px 7px yellow, 8px 8px blue, 9px 9px blue, 10px 10px blue, 11px 11px blue,
      12px 12px blue, 13px 13px blue, 14px 14px red, 15px 15px red,
      16px 16px red, 17px 17px red, 18px 18px red, 19px 19px red, 20px 20px red,
      21px 21px orange, 22px 22px orange, 23px 23px orange, 24px 24px orange,
      25px 25px orange;
  }
  48% {
    text-shadow: 0px 0px transparent, 1px 1px yellow, 2px 2px yellow,
      3px 3px yellow, 4px 4px yellow, 5px 5px yellow, 6px 6px yellow,
      7px 7px blue, 8px 8px blue, 9px 9px blue, 10px 10px blue, 11px 11px blue,
      12px 12px blue, 13px 13px red, 14px 14px red, 15px 15px red, 16px 16px red,
      17px 17px red, 18px 18px red, 19px 19px red, 20px 20px orange,
      21px 21px orange, 22px 22px orange, 23px 23px orange, 24px 24px orange,
      25px 25px orange;
  }
  52% {
    text-shadow: 0px 0px transparent, 1px 1px yellow, 2px 2px yellow,
      3px 3px yellow, 4px 4px yellow, 5px 5px yellow, 6px 6px blue, 7px 7px blue,
      8px 8px blue, 9px 9px blue, 10px 10px blue, 11px 11px blue, 12px 12px red,
      13px 13px red, 14px 14px red, 15px 15px red, 16px 16px red, 17px 17px red,
      18px 18px red, 19px 19px orange, 20px 20px orange, 21px 21px orange,
      22px 22px orange, 23px 23px orange, 24px 24px orange, 25px 25px yellow;
  }
  56% {
    text-shadow: 0px 0px transparent, 1px 1px yellow, 2px 2px yellow,
      3px 3px yellow, 4px 4px yellow, 5px 5px blue, 6px 6px blue, 7px 7px blue,
      8px 8px blue, 9px 9px blue, 10px 10px blue, 11px 11px red, 12px 12px red,
      13px 13px red, 14px 14px red, 15px 15px red, 16px 16px red, 17px 17px red,
      18px 18px orange, 19px 19px orange, 20px 20px orange, 21px 21px orange,
      22px 22px orange, 23px 23px orange, 24px 24px yellow, 25px 25px yellow;
  }
  60% {
    text-shadow: 0px 0px transparent, 1px 1px yellow, 2px 2px yellow,
      3px 3px yellow, 4px 4px blue, 5px 5px blue, 6px 6px blue, 7px 7px blue,
      8px 8px blue, 9px 9px blue, 10px 10px red, 11px 11px red, 12px 12px red,
      13px 13px red, 14px 14px red, 15px 15px red, 16px 16px red,
      17px 17px orange, 18px 18px orange, 19px 19px orange, 20px 20px orange,
      21px 21px orange, 22px 22px orange, 23px 23px yellow, 24px 24px yellow,
      25px 25px yellow;
  }
  64% {
    text-shadow: 0px 0px transparent, 1px 1px yellow, 2px 2px yellow,
      3px 3px blue, 4px 4px blue, 5px 5px blue, 6px 6px blue, 7px 7px blue,
      8px 8px blue, 9px 9px red, 10px 10px red, 11px 11px red, 12px 12px red,
      13px 13px red, 14px 14px red, 15px 15px red, 16px 16px orange,
      17px 17px orange, 18px 18px orange, 19px 19px orange, 20px 20px orange,
      21px 21px orange, 22px 22px yellow, 23px 23px yellow, 24px 24px yellow,
      25px 25px yellow;
  }
  68% {
    text-shadow: 0px 0px transparent, 1px 1px yellow, 2px 2px blue, 3px 3px blue,
      4px 4px blue, 5px 5px blue, 6px 6px blue, 7px 7px blue, 8px 8px red,
      9px 9px red, 10px 10px red, 11px 11px red, 12px 12px red, 13px 13px red,
      14px 14px red, 15px 15px orange, 16px 16px orange, 17px 17px orange,
      18px 18px orange, 19px 19px orange, 20px 20px orange, 21px 21px yellow,
      22px 22px yellow, 23px 23px yellow, 24px 24px yellow, 25px 25px yellow;
  }
  72% {
    text-shadow: 0px 0px transparent, 1px 1px blue, 2px 2px blue, 3px 3px blue,
      4px 4px blue, 5px 5px blue, 6px 6px blue, 7px 7px red, 8px 8px red,
      9px 9px red, 10px 10px red, 11px 11px red, 12px 12px red, 13px 13px red,
      14px 14px orange, 15px 15px orange, 16px 16px orange, 17px 17px orange,
      18px 18px orange, 19px 19px orange, 20px 20px yellow, 21px 21px yellow,
      22px 22px yellow, 23px 23px yellow, 24px 24px yellow, 25px 25px yellow;
  }
  76% {
    text-shadow: 0px 0px transparent, 1px 1px blue, 2px 2px blue, 3px 3px blue,
      4px 4px blue, 5px 5px blue, 6px 6px red, 7px 7px red, 8px 8px red,
      9px 9px red, 10px 10px red, 11px 11px red, 12px 12px red, 13px 13px orange,
      14px 14px orange, 15px 15px orange, 16px 16px orange, 17px 17px orange,
      18px 18px orange, 19px 19px yellow, 20px 20px yellow, 21px 21px yellow,
      22px 22px yellow, 23px 23px yellow, 24px 24px yellow, 25px 25px blue;
  }
  80% {
    text-shadow: 0px 0px transparent, 1px 1px blue, 2px 2px blue, 3px 3px blue,
      4px 4px blue, 5px 5px red, 6px 6px red, 7px 7px red, 8px 8px red,
      9px 9px red, 10px 10px red, 11px 11px red, 12px 12px orange,
      13px 13px orange, 14px 14px orange, 15px 15px orange, 16px 16px orange,
      17px 17px orange, 18px 18px yellow, 19px 19px yellow, 20px 20px yellow,
      21px 21px yellow, 22px 22px yellow, 23px 23px yellow, 24px 24px blue,
      25px 25px blue;
  }
  84% {
    text-shadow: 0px 0px transparent, 1px 1px blue, 2px 2px blue, 3px 3px blue,
      4px 4px red, 5px 5px red, 6px 6px red, 7px 7px red, 8px 8px red,
      9px 9px red, 10px 10px red, 11px 11px orange, 12px 12px orange,
      13px 13px orange, 14px 14px orange, 15px 15px orange, 16px 16px orange,
      17px 17px yellow, 18px 18px yellow, 19px 19px yellow, 20px 20px yellow,
      21px 21px yellow, 22px 22px yellow, 23px 23px blue, 24px 24px blue,
      25px 25px blue;
  }
  88% {
    text-shadow: 0px 0px transparent, 1px 1px blue, 2px 2px blue, 3px 3px red,
      4px 4px red, 5px 5px red, 6px 6px red, 7px 7px red, 8px 8px red,
      9px 9px red, 10px 10px orange, 11px 11px orange, 12px 12px orange,
      13px 13px orange, 14px 14px orange, 15px 15px orange, 16px 16px yellow,
      17px 17px yellow, 18px 18px yellow, 19px 19px yellow, 20px 20px yellow,
      21px 21px yellow, 22px 22px blue, 23px 23px blue, 24px 24px blue,
      25px 25px blue;
  }
  92% {
    text-shadow: 0px 0px transparent, 1px 1px blue, 2px 2px red, 3px 3px red,
      4px 4px red, 5px 5px red, 6px 6px red, 7px 7px red, 8px 8px red,
      9px 9px orange, 10px 10px orange, 11px 11px orange, 12px 12px orange,
      13px 13px orange, 14px 14px orange, 15px 15px yellow, 16px 16px yellow,
      17px 17px yellow, 18px 18px yellow, 19px 19px yellow, 20px 20px yellow,
      21px 21px blue, 22px 22px blue, 23px 23px blue, 24px 24px blue,
      25px 25px blue;
  }
  96% {
    text-shadow: 0px 0px transparent, 1px 1px red, 2px 2px red, 3px 3px red,
      4px 4px red, 5px 5px red, 6px 6px red, 7px 7px red, 8px 8px orange,
      9px 9px orange, 10px 10px orange, 11px 11px orange, 12px 12px orange,
      13px 13px orange, 14px 14px yellow, 15px 15px yellow, 16px 16px yellow,
      17px 17px yellow, 18px 18px yellow, 19px 19px yellow, 20px 20px blue,
      21px 21px blue, 22px 22px blue, 23px 23px blue, 24px 24px blue,
      25px 25px blue;
  }
  100% {
    text-shadow: 0px 0px transparent, 1px 1px red, 2px 2px red, 3px 3px red,
      4px 4px red, 5px 5px red, 6px 6px red, 7px 7px orange, 8px 8px orange,
      9px 9px orange, 10px 10px orange, 11px 11px orange, 12px 12px orange,
      13px 13px yellow, 14px 14px yellow, 15px 15px yellow, 16px 16px yellow,
      17px 17px yellow, 18px 18px yellow, 19px 19px blue, 20px 20px blue,
      21px 21px blue, 22px 22px blue, 23px 23px blue, 24px 24px blue,
      25px 25px red;
  }
}
</style>
