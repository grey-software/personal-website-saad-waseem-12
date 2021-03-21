<template>
  <div class="bg-fixed min-h-screen h-full min-w-full main-background relative p-1 pb-40 md:pb-32">
    <Background/>
    <NavBar class=" relative z-10"/>
    <!-- <div class="bg-white h-full overflow-y-scroll relative"> -->
    <Nuxt class=" relative z-10"/>
    <HoveringSocial class=" relative z-10"/>
    <!-- </div> -->
    <Footer class="absolute bottom-0 right-0 left-0 opacity-75 z-20 mt-6"/>
  </div>
</template>

<script>
export default {};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Pacifico&display=swap");
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;300;600&display=swap');

html,
body {
  min-height: 100vh;
}
.main-background {
  background: rgb(39, 54, 79);
  background: radial-gradient(
    circle,
    rgba(39, 54, 79, 1) 0%,
    rgba(17, 17, 34, 1) 50%,
    rgba(17, 17, 34, 1) 100%
  );
}
</style>
