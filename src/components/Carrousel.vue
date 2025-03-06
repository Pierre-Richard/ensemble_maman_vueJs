<template>
  <v-carousel height="130px">
    <v-carousel-item
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
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
import { Component, Vue } from "vue-facing-decorator";

@Component
export default class Carrousel extends Vue {
  text: string = "";
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style></style>
