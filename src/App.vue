<template>
  <v-app style="
    background: #000000;
  ">
    <v-app-bar app class="black">
      <v-toolbar-title class="headline text-uppercase">
        <p class="mr-5 headerTitle">
          Yuma Shimizu
          <span class="font-weight-light">Portfolio</span>
        </p>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text href="https://github.com/vuetifyjs/vuetify/releases/latest" target="_blank"></v-btn>
    </v-app-bar>
    <v-content>
      <Welcome />
      <Card />
      <Contents />
      <Copylight />
    </v-content>
  </v-app>
</template>

<script>
import Welcome from "./components/Welcome";
import Card from "./components/Card";
import Contents from "./components/Contents";
import Copylight from "./components/Copylight";

export default {
  name: "App",
  components: {
    Welcome,
    Card,
    Contents,
    Copylight
  },
  data: () => ({
    //
  })
};
</script>

<style lang="scss" scoped>
.headerTitle {
  color: #41b883;
}
</style>