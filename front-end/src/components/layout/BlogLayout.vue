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
import AppHeader from "./AppHeader";
import BlogSidebar from "../blog/BlogSidebar";

export default {
  name: "BlogLayout",
  components: {
    AppHeader,
    BlogSidebar
  }
}
</script>

<style scoped>
.wrapper {
  width: 100%;
  height: 100vh;
  background: #F1F3FC;
  overflow: hidden;
}

section {
  width: 100%;
  height: calc(100% - 80px);
  padding: 50px 250px;
  position: relative;
  overflow-y: auto;
}

main {
  margin-left: 20%;
  width: 800px;
  user-select: none;
  -webkit-user-drag: none;
}
</style>