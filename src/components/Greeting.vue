<template>
  <v-container mt-5>
    <v-layout text-center wrap>
      <v-flex xs12 grey--text text--darken-3>
        <h1 class="display-1 grey--text text--darken-3">{{ headline }}</h1>
        <v-card class="mx-auto my-5 py-4" max-width="400">
          <div class="title grey--text text--darken-3">INSTRUCTIONS</div>
          <div>Click the Roll button to roll the dice.</div>
          <div>Each result will be tallied on the scoreboard.</div>
          <div>The first number to get to 5 is the winning number!</div>
          <div>Click the Reset button to start over.</div>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    headline: "Play this dicey Dice Game!!"
  })
};
</script>
