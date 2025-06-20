<template>
  <header class="header">
    <div class="left">
      <font-awesome-icon icon="home" />
      <span>Home</span>
    </div>
    <div class="right">
      <font-awesome-icon icon="user" />
      <template v-if="user">
        <span>{{ user.name }}</span>
      </template>
      <template v-else>
        <SigninButton @login-success="handleLoginSuccess" />
      </template>
    </div>
  </header>
</template>

<script>
import SigninButton from "@/components/SigninButton.vue";

export default {
  name: 'BaseHeader',
  components: { SigninButton },
  data() {
    return {
      user: null
    }
  },
  methods: {
    handleLoginSuccess(user) {
      this.user = user
    }
  }
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
