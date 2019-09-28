<template>
  <v-container my-5>
    <v-layout text-center wrap>
      <v-flex xs12 grey--text text--darken-3>
        <h1 class="display-1">{{ headline }}</h1>
        <h2 class="headline">{{ subtitle }}</h2>
        <v-card class="mx-auto my-5 py-4" max-width="450">
          <div class="title">INSTRUCTIONS</div>
          <v-list-item py-0>
            <v-list-item-content>
              <v-list-item-title
                >Click the Roll button to roll the dice.</v-list-item-title
              >
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                Each result will be tallied on the scoreboard.
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>
                The first number to get to 5 is the winning number!
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title
                >Click the Reset button to start over.</v-list-item-title
              >
            </v-list-item-content>
          </v-list-item>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    headline: "Welcome to Dicey McDiceFace!!",
    subtitle: "The diciest dice game on the Web"
  })
};
</script>
