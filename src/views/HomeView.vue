<template>
  <Header />
  <Text />
</template>

<script lang="ts">
import { Component, toNative, Vue, Watch } from "vue-facing-decorator";

// Components

import Header from "@/components/Header.vue";
import Carrousel from "@/components/Carrousel.vue";
import Text from "@/components/Text.vue";

@Component({
  components: {
    Header,
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
