<template>
  <nav class="nav">
    <div class="logo">
      <img src="../assets/logo.svg" alt="logo" />
    </div>
  </nav>
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
