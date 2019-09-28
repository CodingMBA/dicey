<template>
  <v-layout justify-center>
    <v-simple-table>
      <template v-slot:default>
        <thead>
          <tr>
            <th class="text-left">Number</th>
            <th class="text-left">Count</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(value, name) in counts" :key="name">
            <td>{{ name }}</td>
            <td>{{ value }}</td>
          </tr>
        </tbody>
      </template>
    </v-simple-table>
  </v-layout>
</template>

<script>
export default {
  props: ["counts"]
};
</script>

<style></style>
