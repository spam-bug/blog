<template>
  <button :class="['button', 'button--' + sample]"><slot/></button>
</template>

<script>
export default {
  name: "AppButton",
  props: {
    sample: String
  }
}
</script>

<style scoped>
.button {
  padding: .7em 2em;
  min-width: 120px;
  border: 1px solid transparent;
  border-radius: 4px;
  cursor: pointer;
  user-select: none;
  -webkit-user-drag: none;
}

.button:focus {
  outline: none;
}

.button--default {
  color: #707070;
  background: white;
  border-color: #C4C4C4;
}

.button--default:active {
  color: white;
  background: #15B1F6;
  border-color: #15B1F6;
}
</style>