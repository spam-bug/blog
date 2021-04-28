<template>
  <aside>
    <button>Create new blog</button>
    <SidebarMenu/>
    <ActiveUser/>
  </aside>
</template>

<script>
import SidebarMenu from "./SidebarMenu";
import ActiveUser from "../ActiveUser";

export default {
  name: "Sidebar",
  components: {
    SidebarMenu,
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