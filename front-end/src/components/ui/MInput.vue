<template>
  <div>
    <label>{{ (label) ? label : 'Label' }}</label>
    <input :type="type" :name="name" :placeholder="placeholder">
  </div>
</template>

<script>
export default {
  name: "m-input",
  props: {
    label: String,
    type: String,
    name: String,
    placeholder: String
  }
}
</script>

<style scoped>
div {
  margin: 10px 0px;
}

label {
  display: block;
  font-size: 1.4rem;
  font-weight: 600;
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