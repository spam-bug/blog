<template>
  <label>{{ (label) ? label : 'Label' }}</label>
</template>

<script>
export default {
  name: "AppLabel",
  props: {
    label: String
  }
}
</script>

<style scoped>
label {
  display: block;
  font-size: 1.4rem;
  font-weight: 600;
}
</style>