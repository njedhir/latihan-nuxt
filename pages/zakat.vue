<template>
  <div>
    <v-row>
      <v-col>
        <h2>Kalkulator Zakat</h2>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-card>
          <v-card-title>Box 1</v-card-title>
          <v-card-text>
            Ini isi Box 1
          </v-card-text>
        </v-card>
      </v-col>
      <v-col>
        <v-card>
          <v-card-title>Box 2</v-card-title>
          <v-card-text>
            Ini isi Box 2
          </v-card-text>
        </v-card>
      </v-col>
      <v-col>
        <v-card>
          <v-card-title>Box 3</v-card-title>
          <v-card-text>
            Ini isi Box 3
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-card class="purple lighten-4">
          <v-card-title>Box Bawah 1</v-card-title>
          <v-card-text>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem beatae ex ipsa natus ab dolore quam eius omnis vero voluptas perferendis facilis, iusto incidunt officiis temporibus debitis tempore voluptatem tenetur.
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn icon color="purple"><v-icon>mdi-thumb-up</v-icon></v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col>
        <v-card>
          <v-card-title>Box Bawah 2</v-card-title>
        </v-card>
      </v-col>
    </v-row>
    <v-divider class="my-5"/>
    <v-row>
      <v-col>
        <v-card>
          <v-card-title>
            Hitung Zakat
          </v-card-title>
          <v-card-text>
            <v-row>
              <v-col>
                <v-text-field
                  label="Harta"
                  outlined
                  v-model="harta"
                />
              </v-col>
            </v-row>
            <v-row>
              <v-col>
                Nilai Harta: {{ harta }}
                <br>
                Zakat: {{ zakat }}
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  data: () => ({
    harta: 0
  }),
  methods: {
  },
  computed: {
    zakat() {
      return this.harta * .025
    }
  }
}
</script>