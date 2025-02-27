<template>
  <Carousel />
</template>

<script lang="ts">
import { defineComponent } from "vue";

// Components
import Header from "@/components/Header.vue";
import Carousel from "@/components/Carousel.vue";

export default defineComponent({
  name: "HomeView",

  components: {
    Header,
    Carousel,
  },
});
</script>
