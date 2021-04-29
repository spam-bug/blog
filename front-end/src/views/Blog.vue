<template>
  <BlogLayout>
    <div class="actions">
      <AppButton sample="default">Save to draft</AppButton>
      <AppButton sample="default">Post</AppButton>
    </div>

    <form>
      <AppInput type="text" name="title" label="Title" placeholder="Enter title here..." />
      <BlogTag />
    </form>
  </BlogLayout>
</template>

<script>
import BlogLayout from "../components/layout/BlogLayout";
import AppButton from "../components/ui/AppButton";
import AppInput from "../components/ui/AppInput";
import BlogTag from "../components/blog/BlogTag";

export default {
  name: "Blog",
  components: {
    BlogLayout,
    AppButton,
    AppInput,
    BlogTag
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