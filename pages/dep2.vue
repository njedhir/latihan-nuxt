<template>
  <v-container>
    <v-row>
      <v-col>
        <v-text-field v-model="search"></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <Tabel :list="listSiswa" :headers="tableHeader" :cari="search" />
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
export default {
  layout: 'special',
  data: () => ({
    search: '',
    listSiswa: [
      {
        nama: "Ares",
        hobi: 'Nyantai'
      },
      {
        nama: "Robbi",
        hobi: 'Tenis'
      },
      {
        nama: "Ali",
        hobi: 'Gaming'
      },
      {
        nama: "Nazar",
        hobi: 'Murojaah'
      },
    ],
    tableHeader: [
      { text: "Nama", value: "nama"},
      { text: "Hobi", value: "hobi"},
    ]
  })
}
</script>