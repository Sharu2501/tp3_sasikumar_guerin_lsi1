<template>
  <div class="button-container">
    <!-- Bouton Primaire -->
    <button class="base-button button-primary">
      Primaire
    </button>

    <!-- Bouton Warning -->
    <button class="base-button button-warning">
      Warning
    </button>

    <!-- Bouton Danger -->
    <button class="base-button button-danger">
      Danger
    </button>

    <!-- Bouton Désactivé -->
    <button class="base-button button-disabled" disabled>
      Désactivé
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
  padding: 1rem;
  flex-wrap: wrap;
}

.base-button {
  padding: 12px 24px;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  cursor: pointer;
  transition: all 0.3s ease;
  min-width: 120px;
  text-transform: uppercase;
  font-weight: 500;
  letter-spacing: 0.5px;
}

/* Couleurs et états */
.button-primary {
  background-color: #42b983;
}

.button-warning {
  background-color: #ff9800;
}

.button-danger {
  background-color: #e53935;
}

.button-disabled {
  background-color: #bdbdbd;
  cursor: not-allowed;
}

/* Effets au survol/focus */
.base-button:not(.button-disabled):hover,
.base-button:not(.button-disabled):focus {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.base-button:not(.button-disabled):active {
  transform: translateY(0);
}

/* Effets spécifiques pour chaque bouton */
.button-primary:hover:not(.button-disabled) {
  background-color: #3aa876;
}

.button-warning:hover:not(.button-disabled) {
  background-color: #fb8c00;
}

.button-danger:hover:not(.button-disabled) {
  background-color: #d32f2f;
}
</style>