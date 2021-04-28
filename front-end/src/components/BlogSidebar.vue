<template>
  <aside>
    <button>Create new blog</button>
    <BlogSidebarMenu/>
    <ActiveUser/>
  </aside>
</template>

<script>
import BlogSidebarMenu from "./BlogSidebarMenu";
import ActiveUser from "./ActiveUser";

export default {
  name: "BlogSidebar",
  components: {
    BlogSidebarMenu,
    ActiveUser
  }
}
</script>

<style scoped>
aside {
  width: 150px;
  position: absolute;
}

button {
  font-size: 1.4rem;
  color: white;
  background: #BB943D;
  padding: 5px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:focus {
  outline: none;
}
</style>