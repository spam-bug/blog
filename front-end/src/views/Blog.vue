<template>
  <AppLayout>
    <div class="actions">
      <AppButton sample="default">Save to draft</AppButton>
      <AppButton sample="default">Post</AppButton>
    </div>

    <form>
      <AppInput type="text" name="title" label="Title" placeholder="Enter title here..." />
      <m-tags :tags="tags" />
    </form>
  </AppLayout>
</template>

<script>
import AppLayout from "../layouts/AppLayout";
import AppButton from "../components/ui/AppButton";
import AppInput from "../components/ui/AppInput";
import MTags from "../components/ui/MTags";

export default {
  name: "Blog",
  components: {
    AppLayout,
    AppButton,
    AppInput,
    MTags
  },
  data() {
    return {
      tags: [
        {
          id: 1,
          name: 'Sports'
        },
        {
          id: 2,
          name: 'News'
        },
        {
          id: 3,
          name: 'Editorial'
        },
        {
          id: 4,
          name: 'Weather'
        },
        {
          id: 5,
          name: 'Featured'
        }
      ]
    }
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