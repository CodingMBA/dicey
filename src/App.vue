<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title class="headline ml-2">
        <span class="mr-3 blue--text text--darken-4">DICEY McDICEFACE</span>
      </v-toolbar-title>
      <a href="#">
        <v-img :src="require('./assets/dicey.png')" height="50" width="50" />
      </a>
      <v-spacer></v-spacer>
      <span>
        <a href="https://github.com/CodingMBA?tab=repositories">
          <v-icon class="blue--text text--darken-4">mdi-github-circle</v-icon>
        </a>
      </span>
    </v-app-bar>

    <v-content>
      <Greeting />
      <v-container class="play-area">
        <v-layout row justify-space-around align-center>
          <v-flex md3>
            <Scoreboard :counts="counts" />
          </v-flex>
          <v-flex md3>
            <div class="text-center wrap">
              <div class="mb-6">
                <v-btn @click="roll" class="blue darken-4 white--text mr-5"
                  >Roll</v-btn
                >
                <v-btn @click="resetCount" class="warning">Reset</v-btn>
              </div>
              <div>
                <v-icon
                  v-if="currentRoll"
                  size="6em"
                  class="grey--text text--darken-3"
                  >{{ `mdi-dice-${currentRoll}` }}</v-icon
                >
                <div v-else class="red--text text--darken-3">
                  Click Roll to start.
                </div>
              </div>
            </div>
          </v-flex>
        </v-layout>
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
      this.currentRoll = null;
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

<style lang="scss" scoped>
a {
  text-decoration: none;
}
.play-area {
  max-width: 700px;
}
</style>
