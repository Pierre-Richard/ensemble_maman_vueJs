<template>
  <v-app>
    <v-app-bar :elevation="2">
      <template v-slot:prepend>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
      </template>
      <v-img src="../assets/logo.svg" />
      <v-app-bar-title>Application Bar</v-app-bar-title>
    </v-app-bar>
  </v-app>
</template>

<script lang="ts">
import { Component, Vue, toNative } from "vue-facing-decorator";
@Component
class Header extends Vue {}

export default toNative(Header);
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.nav {
  width: 100%;
  height: 115px;
}

.logo {
  width: 250px;
  height: 113px;
}

img {
  width: 250px;
  height: 113px;
  background-color: yellow;
}
</style>
