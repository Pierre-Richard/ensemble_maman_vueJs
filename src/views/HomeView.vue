<template>
  <Carrousel />
</template>

<script lang="ts">
import { Component, toNative, Vue, Watch } from "vue-facing-decorator";

// Components

import Carrousel from "@/components/Carrousel.vue";
import Text from "@/components/Text.vue";

@Component({
  components: {
    Carrousel,
    Text,
  },
})
export class HomeView extends Vue {
  word: string = "HELLO WORLD";
}
export default toNative(HomeView);
</script>

<style></style>
