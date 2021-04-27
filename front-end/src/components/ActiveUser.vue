<template>
  <div class="container">
    <p>Online 7</p>
    <ActiveUserItem />
  </div>
</template>

<script>
import ActiveUserItem from "./ActiveUserItem";

export default {
  name: "ActiveUser",
  components: {
    ActiveUserItem
  }
}
</script>

<style scoped>
p {
  font-size: 1.2rem;
  color: #707070;
  margin: 10px 0 15px;
}
</style>