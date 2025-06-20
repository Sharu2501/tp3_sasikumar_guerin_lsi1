<script setup>
// import BaseButton from '@/components/BaseButton.vue'
// import AsyncButton from '@/components/AsyncButton.vue'
import SigninButton from '@/components/SigninButton.vue'
</script>

<template>
  <main class="home-page">
    <div class="button-group">
<!--      <BaseButton>Bouton par défaut</BaseButton>-->
<!--    </div>-->
<!--    <p>Here comes the content of the HomePage.</p>-->
<!--    <AsyncButton />-->
    </div>
  </main>
</template>

<script>
export default {
  name: 'HomePage'
}
</script>

<style scoped>
.home-page{
  width: 100%;
  padding: 20px;
  text-align: center;
}

.button-group {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}
</style>
