<template>
  <div class="hello">
    <h1>Vue facing decorator</h1>
  </div>
</template>

<script>
import { Component, Vue, toNative } from "vue-facing-decorator";
@Component
class HelloWorld extends Vue {}

export default toNative(HelloWorld);
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
