<script setup>
import BaseHeader from '@/components/BaseHeader.vue'
import BaseFooter from '@/components/BaseFooter.vue'
</script>

<template>
  <div class="base-layout">
    <BaseHeader />
    <main class="content">
      <slot />
    </main>
    <BaseFooter />
  </div>
</template>

<style scoped>
.base-layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 100%;
}

.content {
  flex: 1;
  padding: 1rem;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
}
</style>