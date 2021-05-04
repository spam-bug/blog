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
      <AppTextArea label="body" name="body" value="Enter text here..." />
    </form>
  </BlogLayout>
</template>

<script>
import BlogLayout from "../components/layout/BlogLayout";
import BlogTag from "../components/blog/BlogTag";
import BlogThumbnail from "../components/blog/BlogThumbnail";
import AppButton from "../components/ui/AppButton";
import AppInput from "../components/ui/AppInput";
import AppTextArea from "../components/ui/AppTextArea";

export default {
  name: "Blog",
  components: {
    BlogLayout,
    BlogTag,
    BlogThumbnail,
    AppButton,
    AppInput,
    AppTextArea
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