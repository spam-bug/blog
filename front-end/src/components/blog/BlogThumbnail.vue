<template>
  <div class="container">
    <AppLabel label="Thumbnail" />
    <p class="note">Upload a picture that represent your post content</p>
    <div class="thumbnail-container">
      <ThumbnailPreview :thumbnail="thumbnail" />
      <div class="action">
        <p class="filename">Filename: {{ thumbnail.name }}</p>
        <UploadButton @preview-thumbnail="previewThumbnail" />
      </div>
    </div>
  </div>
</template>

<script>
import AppLabel from "../ui/AppLabel";
import ThumbnailPreview from "./BlogThumbnailPreview";
import UploadButton from "./BlogThumbnailUploadButton";

export default {
  name: "BlogThumbnail",
  components: {
    AppLabel,
    ThumbnailPreview,
    UploadButton
  },
  data() {
    return {
      thumbnail: {
        name: "",
        image: ""
      }
    }
  },
  methods: {
    previewThumbnail(thumbnail) {
      this.thumbnail.name = thumbnail.name
      this.thumbnail.image = thumbnail.image
    }
  }
}
</script>

<style scoped>
.container {
  margin-top: 15px;
}

.note {
  color: #707070;
  font-size: 1.2rem;
  user-select: none;
  -webkit-user-drag: none;
}

.thumbnail-container {
  display: flex;
  margin-top: 10px;
}

.action {
  margin-left: 20px;
  padding: 10px 0;
  display: flex;
  flex-flow: column;
  justify-content: space-between;
}

.filename {
  font-size: 1.4rem;
  color: #707070;
}
</style>