<template>
  <div>
    <v-row>
      <v-col>
        <v-btn @click="ambilData">Get Data</v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-card>
          <v-data-table
            :headers="tableHeaders"
            :items="depList"
            :loading="tableLoading"
          >
            <!-- <template v-slot="">
              <v-icon @click="deleteData(item.id)">mdi-cross</v-icon>
            </template> -->
          </v-data-table>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  data: () => ({
    tableLoading: false,
    depList: [{
      acid: "SJV332",
      ssrCode: "2315",
      adep: "WIII",
      atd: "2010-07-01T00:00:00.000Z",
      ades: "WARR",
    }],
    tableHeaders: [
      { text: 'ACID', value: 'acid' },
      { text: 'SSR', value: 'ssrCode' },
      { text: 'ADEP', value: 'adep' },
      { text: 'ATD', value: 'atd' },
      { text: 'ADES', value: 'ades' },
      { text: 'Action' },
    ]
  }),
  methods: {
    ambilData() {
      this.tableLoading = true
      this.$axios.get('/aftn/acid')
        .then(response => {
          this.depList = response.data
          this.tableLoading = false
        })
        .catch(err => {
          console.error(err.message)
          this.tableLoading = false
        })
    },
    deleteData(id) {
      this.$axios.delete(`/aftn/acid/${id}`)
        .then(response => {
          if (response.status == 200) {
            const obIndex = this.depList.findIndex(x => x.id == id)
            if (obIndex >= 0) this.depList.splice(obIndex, 1)
          }
        })
        .catch(err => {
          console.error(err.message)
        })
    }
  }
}
</script>
