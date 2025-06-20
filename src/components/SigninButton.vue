<template>
  <button @click="handleSignIn">
    Sign in with Microsoft
  </button>
</template>

<script>
import { signInAndGetUser } from '../lib/microsoftGraph'

export default {
  methods: {
    async handleSignIn() {
      try {
        const user = await signInAndGetUser()
        this.$emit('login-success', user)
      } catch (error) {
        console.error('Login failed:', error)
      }
    }
  }
}
</script>

<style>
button {
  background-color: white;
  color: #26a69a;
  border: none;
  padding: 5px 10px;
  border-radius: 4px;
  cursor: pointer;
  margin-left: 8px;
  font-weight: bold;
}

button:hover {
  background-color: #eeeeee;
}
</style>
