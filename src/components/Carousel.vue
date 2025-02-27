<template>
  <v-card>
    <v-layout>
      <v-app-bar>
        <v-app-bar-nav-icon
          variant="text"
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>
      </v-app-bar>

      <v-navigation-drawer
        v-model="drawer"
        :location="$vuetify.display.mobile ? 'bottom' : undefined"
        temporary
      >
        <v-list :items="data"></v-list>
      </v-navigation-drawer>

      <v-main style="height: 500px">
        <v-card-text>
          The navigation drawer will appear from the bottom on smaller size
          screens.
        </v-card-text>
      </v-main>
    </v-layout>
  </v-card>
</template>

<script lang="ts">
import { Component, Vue, Watch } from "vue-facing-decorator";

@Component
export default class Carousel extends Vue {
  drawer: boolean = true;
  group = null;

  data = [
    {
      title: "Foo",
      value: "foo",
    },
    {
      title: "Bar",
      value: "bar",
    },
    {
      title: "Fizz",
      value: "fizz",
    },
    {
      title: "Buzz",
      value: "buzz",
    },
  ];

  @Watch("drawer")
  onIsOpenChange(newVal: boolean) {
    console.log("newVal", newVal);
    this.drawer = newVal;
  }
}
</script>

<style>
/* .v-carousel {
}
.custom-carousel .v-icon {
  font-size: 18px;
}
.v-btn--icon.v-btn--density-default {
  width: calc(var(--v-btn-height) + 3px);
  height: calc(var(--v-btn-height) + 3px);
} */
</style>
