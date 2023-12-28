<script lang="ts">
import Vue from "vue";
import NavBarA from "./components/NavBarA.vue";
import CarouselSection from "./components/CarouselSection.vue"

export default Vue.extend({
  name: "App",
  components: {
    NavBarA,
    CarouselSection
  },
});
</script>

<template>
  <div id="app">
    <NavBarA />
    <CarouselSection />
  </div>
</template>

<style>

#app {
  font-family: Inter, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

/* width */
::-webkit-scrollbar {
  width: 5px;
}

</style>
