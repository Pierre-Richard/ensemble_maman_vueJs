<template>
  <v-card>
    <v-layout>
      <v-app-bar>
        <v-img :width="179" src="./assets/logo.svg" />
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
          </v-list-item-group> </v-list
        >>
      </v-navigation-drawer>
    </v-layout>
  </v-card>
</template>
<script lang="ts">
import { Component, toNative, Vue, Watch } from "vue-facing-decorator";
interface tab {
  icon: string;
  title: string;
  route: string;
}
@Component({
  components: {},
})
export class App extends Vue {
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

  items: tab[] = [
    { icon: "mdi-speedometer", title: "home", route: "/" },
    { icon: "mdi-tools", title: "about", route: "/about" },
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
export default toNative(App);
</script>
<style>
* {
  margin: 0;
  padding: 0;
}
</style>
