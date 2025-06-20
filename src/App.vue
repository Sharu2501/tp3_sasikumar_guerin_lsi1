<template>
  <div id="app">
    <BaseLayout>
    <main class="main-content">
      <HomePage />
    </main>
    </BaseLayout>
  </div>
</template>

<script>
import BaseLayout from '@/components/BaseLayout.vue'
import HomePage from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    BaseLayout,
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
