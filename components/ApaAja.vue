<template>
  <div>
    <v-text-field
      outlined
      v-model="isian"
    />
    <v-btn @click="klikTombol">Push Me</v-btn>
  </div>
</template>
<script>
export default {
  props: [],
  data: () => ({
    isian: ''
  }),
  methods: {
    klikTombol() {
      this.$emit('klik', this.isian)
    }
  }
}
</script>