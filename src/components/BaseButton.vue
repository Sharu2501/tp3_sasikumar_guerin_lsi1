<template>
  <div class="button-container">
    <!-- Bouton actif avec animation -->
    <button class="base-button custom-margin animated-button">
      Bouton actif
    </button>

    <!-- Bouton désactivé -->
    <button class="base-button" disabled>
      Bouton désactivé
    </button>
  </div>
</template>

<script>
export default {
  name: 'BaseButton'
}
</script>

<style scoped>
.button-container {
  display: flex;
  gap: 1rem;
}

.base-button {
  padding: 10px 20px;
  background-color: #26a69a;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.2s ease;
}

.base-button:hover:enabled,
.base-button:focus:enabled {
  background-color: #2bbbad;
}

.base-button:disabled {
  background-color: #8bc584;
  cursor: not-allowed;
}

.custom-margin {
  margin: 20px;
}

/* Animation sur hover et focus */
.animated-button:hover,
.animated-button:focus {
  transform: scale(1.05);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}
</style>
