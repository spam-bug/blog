<template>
  <div>
    <div v-for="tag in tags" :key="tag.id">
      <input type="radio" name="tag">
      <button>{{ tag.name }}</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Mtags",
  props: {
    tags: Array
  }
}
</script>

<style scoped>

</style>