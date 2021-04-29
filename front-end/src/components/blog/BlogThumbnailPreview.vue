<template>
  <div class="thumbnail">
    <span class="material-icons-outlined" v-if="!thumbnail.image">image</span>
    <img v-if="thumbnail.image" :src="thumbnail.image" :alt="thumbnail.name">
  </div>
</template>

<script>
export default {
  name: "BlogThumbnailPreview",
  props: {
    thumbnail: Object
  }
}
</script>

<style scoped>
.thumbnail {
  width: 150px;
  height: 100px;
  background: white;
  border: 1px solid #C4C4C4;
  border-radius: 4px;
  position: relative;
  overflow: hidden;
}

span {
  position: absolute;
  color: #C4C4C4;
  font-size: 5rem;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  user-select: none;
}

img {
  width: 150px;
  height: 100px;
  object-fit: cover;
  object-position: center;
  user-select: none;
  -webkit-user-drag: none;
}

</style>