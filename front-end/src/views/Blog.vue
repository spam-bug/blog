<template>
  <AppLayout>
    <div class="actions">
      <m-button sample="default">Save to draft</m-button>
      <m-button sample="default">Post</m-button>
    </div>

    <form>
      <m-input type="text" name="title" label="Title" placeholder="Enter title here..." />
    </form>
  </AppLayout>
</template>

<script>
import AppLayout from "../layouts/AppLayout";
import MButton from "../components/ui/MButton";
import MInput from "../components/ui/MInput";

export default {
  name: "Blog",
  components: {
    AppLayout,
    MButton,
    MInput
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