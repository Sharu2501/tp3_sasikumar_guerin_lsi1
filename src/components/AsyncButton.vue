<script setup>
import { ref } from 'vue'

const isPending = ref(false)
const clickCount = ref(0)

const handleClick = () => {
  if (isPending.value) return

  isPending.value = true
  const delay = 1000 + (clickCount.value * 1000)
  clickCount.value++

  setTimeout(() => {
    isPending.value = false
  }, delay)
}
</script>

<template>
  <button
      class="async-button"
      :class="{ 'button-disabled': isPending }"
      :disabled="isPending"
      @click="handleClick"
  >
    <span v-if="!isPending">Disabled and animated for 2 seonds if clicked</span>
    <span v-else class="loading-text">
      <span class="loading-dots">.</span>
      <span class="loading-dots">.</span>
      <span class="loading-dots">.</span>
    </span>
  </button>
</template>

<style scoped>
.async-button {
  padding: 12px 24px;
  background-color: #42b983;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  cursor: pointer;
  transition: all 0.3s ease;
  min-width: 150px;
}

.async-button:hover:not(.button-disabled) {
  background-color: #3aa876;
  transform: translateY(-2px);
}

.async-button:active:not(.button-disabled) {
  transform: translateY(0);
}

.button-disabled {
  background-color: #bdbdbd;
  cursor: not-allowed;
}

.loading-text {
  display: inline-flex;
  gap: 2px;
}

.loading-dots {
  animation: pulse 1.5s infinite ease-in-out;
}

.loading-dots:nth-child(2) {
  animation-delay: 0.2s;
}

.loading-dots:nth-child(3) {
  animation-delay: 0.4s;
}

@keyframes pulse {
  0%, 100% { opacity: 0.3; }
  50% { opacity: 1; }
}
</style>