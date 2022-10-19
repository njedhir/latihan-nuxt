<template>
  <v-card>
    <v-data-table
      :headers="headers"
      :items="list"
      :search="cari"
    ></v-data-table>
    </v-card>
</template>
<script>
export default {
  props: [
    'list',
    'headers',
    'cari'
  ]
}
</script>
