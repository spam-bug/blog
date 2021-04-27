<template>
  <div class="wrapper">
    <AppHeader/>
    <section>
      <BlogSidebar/>
    </section>
  </div>
</template>

<script>
import AppHeader from "../components/AppHeader";
import BlogSidebar from "../components/BlogSidebar";

export default {
  name: "AppLayout",
  components: {
    AppHeader,
    BlogSidebar
  }
}
</script>

<style scoped>
.wrapper {
  width: 100%;
  min-height: 100vh;
  background: #F1F3FC;
}

section {
  width: 100%;
  padding: 50px 350px;
  position: relative;
}
</style>