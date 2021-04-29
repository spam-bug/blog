<template>
  <div>
    <AppLabel :label="label" />
    <input :type="type" :name="name" :placeholder="placeholder">
  </div>
</template>

<script>
import AppLabel from "./AppLabel";

export default {
  name: "AppInput",
  props: {
    label: String,
    type: String,
    name: String,
    placeholder: String
  },
  components: {
    AppLabel
  }
}
</script>

<style scoped>
div {
  margin: 10px 0px;
}

input {
  width: 100%;
  padding: 10px;
  border: 1px solid #C4C4C4;
  border-radius: 4px;
  margin-top: 5px;
}

input:focus {
  outline-color: #15B1F6;
}
</style>