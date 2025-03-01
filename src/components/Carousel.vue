<template>
  <v-card>
    <v-layout>
      <v-app-bar class="text" color="red">
        <v-img :width="179" src="../assets/logo.svg" />
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
    </v-layout>
  </v-card>
  <!-- <v-text-field
    label="Label"
    v-model="textInput"
    variant="solo-filled"
  ></v-text-field>
  <v-btn variant="outlined" @click="clickOnButton()"> Button </v-btn>
  <span>{{ textInput }}</span> -->
</template>

<script lang="ts">
import { Component, Vue, Watch } from "vue-facing-decorator";

@Component
export default class Carousel extends Vue {
  textInput: string = "";
  drawer: boolean = false;
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
    console.log("InputText", this.textInput);
    this.drawer = newVal;
  }

  clickOnButton() {
    //comment en click sur mon button je peux recuperer
    // la valeur de mon formulaire
    console.log("Je click sur le button", this.textInput);
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
  width: calc(var(--v-btn-height) + 3px)
  height: calc(var(--v-btn-height) + 3px);
} */
</style>
