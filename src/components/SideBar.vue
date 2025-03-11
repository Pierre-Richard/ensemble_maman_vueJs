<template>
  <v-navigation-drawer
    v-model="drawer"
    :location="$vuetify.display.mobile ? 'bottom' : undefined"
    temporary
  >
    <v-list flat dense nav class="py-1">
      <v-list-item-group color="primary" mandatory>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          dense
          router
          :to="item.route"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-title>{{ item.title }}</v-list-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-navigation-drawer>
</template>

<script lang="ts">
import { Component, Vue, toNative, Prop } from "vue-facing-decorator";
@Component
export class SieBar extends Vue {
  @Prop({ default: false, type: Boolean }) isDrawer?: boolean;
}
export default toNative(SieBar);
</script>

<style></style>
