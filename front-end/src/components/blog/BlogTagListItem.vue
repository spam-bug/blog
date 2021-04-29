<template>
  <div>
    <input type="radio" name="tag" :checked="selectedTag === tag.id" value="{{ tag.name }}">
    <span @click="$emit('select-tag', tag.id)" :class="[(selectedTag === tag.id) ? 'selected' : '']">{{ tag.name }}</span>
  </div>
</template>

<script>

export default {
  name: "BlogTagListItem",
  props: {
    tag: Object,
    selectedTag: Number
  }
}
</script>

<style scoped>
div {
  margin-right: 10px;
}

input {
  display: none
}

span {
  font-size: 1.4rem;
  padding: 5px 15px;
  color: #707070;
  background: white;
  border: 1px solid #C4C4C4;
  border-radius: 4px;
  cursor: pointer;
  user-select: none;
}

span.selected {
  color: white;
  background: #15B1F6;
  border-color: #15B1F6;
}
</style>