<template>
  <div class="wrapper">
    <AppHeader/>
    <section>
      <BlogSidebar/>
      <main>
        <slot/>
      </main>
    </section>
  </div>
</template>

<script>
import AppHeader from "../components/layout/AppHeader";
import BlogSidebar from "../components/blog/Sidebar";

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
  padding: 50px 250px;
  position: relative;
}

main {
  margin-left: 200px;
  width: 800px;
}
</style>