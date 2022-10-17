<template>
  <v-simple-table>
    <thead>
      <tr>
        <th>Nama</th>
        <th>Hobi</th>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="(siswa, index) in listSiswa"
        :key="index"
      >
        <td>{{siswa.nama}}</td>
        <td>{{siswa.hobi}}</td>
      </tr>
    </tbody>
  </v-simple-table>
</template>
<script>
export default {
  data: () => ({
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
    ]
  })
}
</script>