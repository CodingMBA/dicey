<template>
  <div class="text-center">
    <v-dialog v-model="dialog" width="500">
      <v-card>
        <v-card-title class="headline grey lighten-2" primary-title>
          {{ `#${currentRoll} is the Winner!!` }}
        </v-card-title>
        <v-card-text class="subtitle-1 blue--text text--darken-2 mt-4"
          >Would you like to play again?</v-card-text
        >
        <v-divider></v-divider>
        <v-card-actions>
          <div class="flex-grow-1"></div>
          <v-btn color="#0053a4" text @click="$emit('reset')">Yes</v-btn>
          <v-btn color="#D50000" text @click="dialog = false">No</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      dialog: false
    };
  },
  props: {
    currentRoll: String,
    dialog: Boolean
  }
};
</script>
