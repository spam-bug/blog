<template>
  <AppLayout>
    <div>
      <Button type="default">Save to draft</Button>
      <Button type="default">Post</Button>
    </div>
  </AppLayout>
</template>

<script>
import AppLayout from "../layouts/AppLayout";
import Button from "../components/ui/Button";

export default {
  name: "Blog",
  components: {
    Button,
    AppLayout
  }
}
</script>

<style scoped>

</style>