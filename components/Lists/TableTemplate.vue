<script setup lang="ts">
const data = {
  header: ["model", "mpg", "hp", "gear", "seats"],
  values: [
    ["Mazda RX4", 21.0, 110, 4, 2],
    ["Mazda RX4 Wag", 21.0, "NA", 4, 5],
    ["Datsun 710", 22.8, 93, 4, 2],
    ["Hornet 4 Drive", 21.4, 110, 3, 2],
    ["Valiant", 18.1, 105, 3, 2],
  ],
};
</script>
<template>
  <div class="relative overflow-x-auto">
    <table>
      <thead>
        <tr>
          <th v-for="heading in data.header" scope="col">
            {{ heading }}
          </th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="row in data.values">
          <th scope="row">{{ row[0] }}</th>
          <td v-for="i in row.length">{{ row[i] }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped lang="postcss">
table {
  @apply w-full text-left text-sm text-gray-500 dark:text-gray-400;
}
thead {
  @apply border-b-4 text-xs uppercase text-gray-700 dark:bg-gray-700 dark:text-gray-400;
}
thead > tr > th {
  @apply py-3 px-6;
}
tbody > tr {
  @apply border-b bg-white dark:border-gray-700 dark:bg-gray-800;
}
tbody > tr > th {
  @apply whitespace-nowrap py-4 px-6 font-medium text-gray-900 dark:text-white;
}
tbody > tr > td {
  @apply py-4 px-6;
}
</style>
