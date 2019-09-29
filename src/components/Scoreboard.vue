<template>
  <v-layout class="pl-4">
    <v-simple-table>
      <template v-slot:default>
        <thead>
          <tr>
            <th class="text-left subtitle-2 blue--text text--darken-4">
              Number
            </th>
            <th class="text-left subtitle-2 blue--text text--darken-4">
              Count
            </th>
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
