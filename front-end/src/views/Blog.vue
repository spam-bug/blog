<template>
  <BlogLayout>
    <div class="actions">
      <AppButton sample="default">Save to draft</AppButton>
      <AppButton sample="default">Post</AppButton>
    </div>

    <form v-on:submit.prevent>
      <AppInput type="text" name="title" label="Title" placeholder="Enter title here..." />
      <BlogTag />
      <BlogThumbnail />
    </form>
  </BlogLayout>
</template>

<script>
import BlogLayout from "../components/layout/BlogLayout";
import AppButton from "../components/ui/AppButton";
import AppInput from "../components/ui/AppInput";
import BlogTag from "../components/blog/BlogTag";
import BlogThumbnail from "../components/blog/BlogThumbnail";

export default {
  name: "Blog",
  components: {
    BlogLayout,
    AppButton,
    AppInput,
    BlogTag,
    BlogThumbnail
  }
}
</script>

<style scoped>
.actions {
  display: flex;
  justify-content: flex-end;
}

.actions button {
  margin-left: 10px;
}
</style>