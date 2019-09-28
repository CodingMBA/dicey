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
      <v-container class="grey lighten-5">
        <v-row class="align-center">
          <v-col>
            <Scoreboard :counts="counts" />
          </v-col>
          <v-col class="text-center">
            <div v-if="currentRoll === 1">
              <v-icon size="6em">mdi-dice-1</v-icon>
            </div>
            <div v-else-if="currentRoll === 2">
              <v-icon size="6em">mdi-dice-2</v-icon>
            </div>
            <div v-else-if="currentRoll === 3">
              <v-icon size="6em">mdi-dice-3</v-icon>
            </div>
            <div v-else-if="currentRoll === 4">
              <v-icon size="6em">mdi-dice-4</v-icon>
            </div>
            <div v-else-if="currentRoll === 5">
              <v-icon size="6em">mdi-dice-5</v-icon>
            </div>
            <div v-else-if="currentRoll === 6">
              <v-icon size="6em">mdi-dice-6</v-icon>
            </div>
            <div v-else>Click the Roll button to start.</div>
          </v-col>
          <v-col>
            <v-btn @click="roll" class="primary mr-5">Roll</v-btn>
            <v-btn @click="resetCount" class="warning">Reset</v-btn>
          </v-col>
        </v-row>
      </v-container>
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
  data: () => {
    return {
      currentRoll: null,
      counts: {
        1: 0,
        2: 0,
        3: 0,
        4: 0,
        5: 0,
        6: 0
      }
    };
  },
  methods: {
    roll() {
      this.currentRoll = Math.floor(Math.random() * 6) + 1;
      this.counts[this.currentRoll] += 1;
    },
    resetCount() {
      this.counts = {
        1: 0,
        2: 0,
        3: 0,
        4: 0,
        5: 0,
        6: 0
      };
    }
  }
};
</script>
