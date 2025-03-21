<template>
  <v-carousel height="300px">
    <v-carousel-item
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
      title="Nous les mamans"
      cover
    ></v-carousel-item>

    <v-carousel-item
      src="https://cdn.vuetifyjs.com/images/cards/hotel.jpg"
      cover
    ></v-carousel-item>

    <v-carousel-item
      src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
      cover
    ></v-carousel-item>
  </v-carousel>
</template>

<script lang="ts">
import { Component, Vue, toNative } from "vue-facing-decorator";

@Component
export class Carrousel extends Vue {
  text: string = "";
}
export default toNative(Carrousel);
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style></style>
