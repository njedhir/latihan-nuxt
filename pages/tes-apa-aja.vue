<template>
  <ApaAja v-on:klik="komponenKlik" />
</template>
<script>
export default {
  data: () => ({

  }),
  methods: {
    komponenKlik(isian) {
      alert(isian)
    }
  }
}
</script>