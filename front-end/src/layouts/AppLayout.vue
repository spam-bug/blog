<template>
  <div class="wrapper">
    <AppHeader/>
  </div>
</template>

<script>
import AppHeader from "../components/AppHeader";

export default {
  name: "AppLayout",
  components: {
    AppHeader
  }
}
</script>

<style scoped>
.wrapper {
  width: 100%;
  min-height: 100vh;
  background: #F1F3FC;
}
</style>