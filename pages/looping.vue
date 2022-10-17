<template>
  <div>
    <v-card
      class="mb-5"
      v-for="(siswa, index) in listSiswa"
      :key="index"
      :color="apakahNazar(siswa.nama)"
    >
      <v-card-title>
        {{ siswa.nama }}
      </v-card-title>
      <v-card-text>
        Hobi: {{ siswa.hobi }}
        
      </v-card-text>
    </v-card>
  </div>
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
  }),
  methods: {
    apakahNazar(nama) {
      return nama == 'Nazar' ? 'purple lighten-4' : ''
    }
  }
}

</script>