<template>
  <div>{{ mot }}</div>
</template>

<script lang="ts">
import { Component, toNative, Vue } from "vue-facing-decorator";
@Component
export class Text extends Vue {
  mot: string = "CA va marcher mtn";
}
export default toNative(Text);
</script>

<style></style>
