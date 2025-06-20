<template>
  <div id="app">
    <BaseHeader />
    <main class="main-content">
      <HomePage />
    </main>
    <BaseFooter />
  </div>
</template>

<script>
import BaseHeader from './components/BaseHeader.vue'
import BaseFooter from './components/BaseFooter.vue'
import HomePage from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    BaseHeader,
    BaseFooter,
    HomePage
  }
}
</script>

<style>
html, body, #app {
  height: 100%;
  margin: auto;
  background-color: white;
  color : black;
}

#app {
  display: flex;
  flex-direction: column;
  width: 100%;
  box-sizing: border-box;
}

.main-content {
  width: 100%;
  flex: 1;
  padding: 20px;
}
</style>
