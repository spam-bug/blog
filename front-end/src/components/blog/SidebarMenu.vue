<template>
  <ul class="menu">
    <li class="menu__item"><a href="#" class="item__link">All blogs</a></li>
    <li class="menu__item"><a href="#" class="item__link">My blogs</a></li>
    <li class="menu__item"><a href="#" class="item__link">Drafts</a></li>
    <li class="menu__item"><a href="#" class="item__link">Pending</a></li>
    <li class="menu__item"><a href="#" class="item__link">Trash</a></li>
  </ul>
</template>

<script>
export default {
  name: "SidebarMenu"
}
</script>

<style scoped>
.menu {
  display: block;
  padding: 20px 0;
  border-bottom: 1px solid #C4C4C4;
}

.menu__item {
  padding: 5px 0px;
}

.item__link {
  font-size: 1.4rem;
  color: #707070;
}

.item__link:hover,
.item__link.active{
  font-weight: bold;
  color: black
}

</style>