<template>
  <div>
    <AppLabel :label="label" />
    <div class="grow-wrap">
      <textarea :name="name"
                v-model="currentValue"
                @focusin="clearDefault"
                @focusout="setDefault"
                oninput="this.parentNode.dataset.replicatedValue  = this.value">
      </textarea>
    </div>
  </div>
</template>

<script>
import AppLabel from "./AppLabel";

export default {
  name: "AppTextArea",
  props: {
    label: String,
    name: String,
    value: {
      required: false,
      type: String,
      default: ''
    }
  },
  components: {
    AppLabel
  },
  data() {
    return {
      currentValue: this.value
    }
  },
  methods: {
    clearDefault(e) {
      if(e.target.value === this.value) {
        this.currentValue = ""
      }
    },
    setDefault(e) {
      if(e.target.value === "") {
        this.currentValue = this.value
      }
    }
  }
}
</script>

<style scoped>
div {
  margin-top: 10px;
}

.grow-wrap {
  display: grid;
}

.grow-wrap::after {
  content: attr(data-replicated-value) " ";
  white-space: pre-wrap;
  visibility: hidden;
}

.grow-wrap > textarea {
  resize: none;
  overflow: hidden;
}

.grow-wrap > textarea,
.grow-wrap::after{
  width: 100%;
  min-height: 200px;
  padding: 10px;
  border: 1px solid #C4C4C4;
  border-radius: 4px;
  grid-area: 1 / 1 / 2 / 2;
  margin-top: 5px;
  outline-color: #15B1F6;
}
</style>