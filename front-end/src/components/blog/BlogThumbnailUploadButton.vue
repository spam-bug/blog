<template>
  <div>
    <input type="file" ref="file" name="thumbnail" @change="convertToBase64" accept="image/jpeg">
    <button @click="$refs.file.click()">Upload</button>
  </div>
</template>

<script>
export default {
  name: "BlogThumbnailUploadButton",
  data() {
    return {
      thumbnail: {
        name: "",
        image: ""
      }
    }
  },
  methods: {
    convertToBase64(e) {
      const selectedImage = e.target.files[0]

      if (!selectedImage) return // no image selected
      if (!this.isJpeg(selectedImage)) return // throw error if not jpeg

      const reader = new FileReader()

      reader.onload = (e) => {
        this.thumbnail.name = selectedImage.name
        this.thumbnail.image = e.target.result
        this.$emit('preview-thumbnail', this.thumbnail)
      }

      reader.readAsDataURL(selectedImage)

    },

    isJpeg(image) {
      const extension = image.name.split('.').slice(-1)[0]

      if(extension === 'jpeg' || extension === 'jpg') return true

      return false
    }
  }
}
</script>

<style scoped>
input {
  display: none;
}

button {
  padding: 5px 25px;
  color: #707070;
  background: white;
  border: 1px solid #C4C4C4;
  border-radius: 4px;
  cursor: pointer;
  user-select: none;
  -webkit-user-drag: none;
}

button:active {
  color: white;
  background: #15B1F6;
  border-color: #15B1F6;
}
</style>