<template>
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view /> -->
  <HomeView />
</template>
<script lang="ts">
import { defineComponent } from "vue";
import HomeView from "./views/HomeView.vue";
import Carousel from "./components/Carousel.vue";

export default defineComponent({
  name: "App",

  components: {
    HomeView,
    Carousel,
  },
});
</script>
<style>
* {
  margin: 0;
  padding: 0;
}
</style>
