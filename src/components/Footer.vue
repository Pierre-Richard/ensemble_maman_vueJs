<template>
  <v-footer
    class="d-flex align-center justify-center ga-2 flex-wrap flex-grow-1 py-3"
    color="surface-light"
    height="120px"
  >
    <div class="flex-1-0-100 text-center mt-2">
      <strong>© copyright Ensemble Mamans </strong>
      {{ new Date().getFullYear() }}
    </div>
  </v-footer>
</template>

<script>
import { Component, toNative, Vue } from "vue-facing-decorator";
@Component
export class Footer extends Vue {}
export default toNative(Footer);
</script>

<style lang="scss" scoped></style>
