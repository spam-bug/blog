<template>
  <button :class="['btn', 'btn-' + sample]"><slot/></button>
</template>

<script>
export default {
  name: "m-button",
  props: {
    sample: String
  }
}
</script>

<style scoped>
.btn {
  padding: .7em 2em;
  min-width: 120px;
  border: 1px solid transparent;
  border-radius: 4px;
  cursor: pointer;
}

.btn:focus {
  outline: none;
}

.btn-default {
  color: #707070;
  background: white;
  border-color: #C4C4C4;
}

.btn-default:active {
  color: white;
  background: #15B1F6;
  border-color: #15B1F6;
}
</style>