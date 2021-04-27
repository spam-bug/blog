<template>
  <header>
    <div class="brand">
      <AppLogo class="brand__logo" />
      <h1 class="brand__name">The Guilds</h1>
    </div>
    <div class="actions">
      <span class="material-icons-outlined">mail_outline</span>
      <span class="material-icons-outlined">notifications</span>
        <img class="avatar" src="https://images.pexels.com/photos/614810/pexels-photo-614810.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260" alt="">
    </div>
  </header>
</template>

<script>
import AppLogo from "./AppLogo";

export default {
  name: "AppHeader",
  components: {
    AppLogo
  }
}
</script>

<style scoped>
header {
  width: 100%;
  padding: 15px 50px;
  background: white;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-shadow: 0 3px 6px 0 rgba(0,0,0,0.25);
}

.brand {
  display: flex;
  align-items: center;
}

.brand__logo {
  width: 60px;
}

.brand__name {
  font-family: Serif;
  font-size: 3rem;
  color: #BB943D;
  margin-left: 20px;
}

.actions {
  display: flex;
  align-items: center;
}

.actions span {
  margin: 0 10px;
}

.avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  object-fit: cover;
  vertical-align: center;
}
</style>