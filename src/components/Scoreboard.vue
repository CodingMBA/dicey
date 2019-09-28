<template>
  <v-layout text-center wrap mt-5>
    <v-flex xs12 mb-5>
      <h2 class="headline font-weight-bold mb-3">Counts by Number</h2>
      <v-layout justify-center>
        <div
          v-for="(number, i) in numberCounts"
          :key="i"
          class="subheading mx-3"
        >
          <p>{{ number.number }}</p>
          <p>{{ number.count }}</p>
        </div>
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data: () => ({
    numberCounts: [
      {
        number: "One",
        count: 0
      },
      {
        number: "Two",
        count: 0
      },
      {
        number: "Three",
        count: 0
      },
      {
        number: "Four",
        count: 0
      },
      {
        number: "Five",
        count: 0
      },
      {
        number: "Six",
        count: 0
      }
    ]
  })
};
</script>

<style></style>
