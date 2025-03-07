<template>
  <div>{{ mot }}</div>
</template>

<script lang="ts">
import { Vue, Watch, Component, toNative } from "vue-facing-decorator";

@Component
export class About extends Vue {
  mot: string = "je suis sur la page About";
}
export default toNative(About);
</script>

<style></style>
