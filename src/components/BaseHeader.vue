<template>
  <header class="header">
    <div class="left">
      <font-awesome-icon icon="home" />
      <span>Home</span>
    </div>
    <div class="right">
      <font-awesome-icon icon="user" />
      <span>Not yet logged-in</span>
    </div>
  </header>
</template>

<script>
export default {
  name: 'BaseHeader'
}
</script>

<style scoped>
.header {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #26a69a;
  color: white;
  padding: 10px 20px;
}
.left, .right {
  display: flex;
  align-items: center;
}
.left span, .right span {
  margin-left: 8px;
}
</style>
