<template>
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view /> -->
  <HomeView />
</template>
<script lang="ts">
import { Component, toNative, Vue, Watch } from "vue-facing-decorator";
import HomeView from "./views/HomeView.vue";

@Component({
  components: {
    HomeView,
  },
})
export class App extends Vue {}
export default toNative(App);
</script>
<style>
* {
  margin: 0;
  padding: 0;
}
</style>
