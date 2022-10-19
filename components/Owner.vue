<template>
  <v-card color="purple lighten-4">
    <v-card-text class="text-center">
      <v-row>
        <v-col>
          <v-btn
            icon
            outlined
          ><v-icon>mdi-account</v-icon></v-btn>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <h1>{{nama}}</h1>
          <br>
          <h2>{{posisi}}</h2>
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>
<script>
export default {
  props: ['nama', 'posisi'],
  data: () => ({
  })
}
</script>