<template>
  <div>
    <div class="user">
      <img src="https://images.pexels.com/photos/614810/pexels-photo-614810.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260" alt="avatar" class="user__avatar">
      <div class="user__details">
        <h3 class="name">Jane Doe</h3>
        <p class="title">admin</p>
      </div>
    </div>
    <div class="user">
      <img src="https://images.pexels.com/photos/614810/pexels-photo-614810.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260" alt="avatar" class="user__avatar">
      <div class="user__details">
        <h3 class="name">Jane Doe</h3>
        <p class="title">admin</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ActiveUserItem"
}
</script>

<style scoped>
.user {
  width: 140px;
  display: flex;
  margin: 15px 0px;
  cursor: pointer;
}

.user__avatar {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  object-fit: cover;
  vertical-align: center;
}
.user__details {
  padding: 5px 10px;
}

.name {
  margin-bottom: 3px;
}

.title {
  color: #707070;
}
</style>