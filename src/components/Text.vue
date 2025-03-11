<template>
  <div>{{ titreProps }}</div>
</template>

<script lang="ts">
import { Component, Prop, toNative, Vue } from "vue-facing-decorator";
@Component
export class Text extends Vue {
  @Prop({ default: "Je suis une Props dans le SideBar" }) titreProps?: string;
  mot: string = "CA va marcher mtn";
}
export default toNative(Text);
</script>

<style></style>
