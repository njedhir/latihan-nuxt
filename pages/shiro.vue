<template>
  <div>
    <p>Hey.. This is {{nama}}'s page</p>
    <v-btn
      elevation="3"
      class="pa-15 mt-5"
      @click="gantiNama"
    >Ganti Nama</v-btn>
  </div>
</template>
<script>
export default {
  data: () => ({
    nama: 'Shiro'
  }),
  methods: {
    gantiNama() {
      if (this.nama == 'Shiro') {
        this.nama = 'Ares'
      } else {
        this.nama = 'Shiro'
      }
    }
  }
}
</script>