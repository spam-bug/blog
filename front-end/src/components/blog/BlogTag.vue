<template>
  <div>
    <AppLabel label="Tags"/>
    <BlogTagList/>
  </div>
</template>

<script>
import AppLabel from "../ui/AppLabel";
import BlogTagList from "./BlogTagList";

export default {
  name: "BlogTag",
  components: {
    AppLabel,
    BlogTagList
  }
}
</script>

<style scoped>

</style>