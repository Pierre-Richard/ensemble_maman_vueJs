<template>
  <div class="hello">
    <h1>Composant Header</h1>
  </div>
</template>

<script lang="ts">
import { Component, Vue, toNative } from "vue-facing-decorator";
@Component
class Header extends Vue {}

export default toNative(Header);
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
