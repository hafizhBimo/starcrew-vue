<script setup>
import { RouterView } from 'vue-router';
import FooterCustom from './components/ui/FooterCustom.vue';
</script>

<template>
  <div class="app-wrapper">
    <main class="main-content">
      <RouterView />
    </main>
    <FooterCustom />
  </div>
</template>

<style scoped lang="scss">
.app-wrapper {
  display: flex;
  flex-direction: column;
  min-height: 100vh; // Ensures full height
}

.main-content {
  flex: 1; // Pushes footer down when content is small
  display: flex;
  flex-direction: column;
}
</style>
