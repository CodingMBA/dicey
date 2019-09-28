<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title class="headline ml-2">
        <span class="font-weight-light mr-2">DICEY McDICEFACE</span>
      </v-toolbar-title>
      <a href="#">
        <v-img :src="require('./assets/dicey.png')" height="50" width="50" />
      </a>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">
          <v-icon>mdi-github-circle</v-icon>
        </span>
      </v-btn>
    </v-app-bar>

    <v-content>
      <Greeting />
      <Scoreboard />
    </v-content>
  </v-app>
</template>

<script>
import Greeting from "./components/Greeting";
import Scoreboard from "./components/Scoreboard";

export default {
  name: "App",
  components: {
    Greeting,
    Scoreboard
  },
  data: () => ({
    //
  })
};
</script>
