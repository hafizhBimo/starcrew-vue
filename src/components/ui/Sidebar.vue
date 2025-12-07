<template>
  <aside
    class="sidebar h-full w-full bg-white shadow-lg border-r flex flex-col p-4"
  >
    <h2 class="text-xl font-bold mb-6">StarCrew</h2>

    <nav class="flex flex-col gap-4">
      <RouterLink to="/" class="nav-item" active-class="active">
        🏠 Feed
      </RouterLink>

      <RouterLink to="/fanart" class="nav-item" active-class="active">
        🎨 Fan Art
      </RouterLink>

      <RouterLink to="/coming-soon" class="nav-item" active-class="active">
        ✨ Coming Soon
      </RouterLink>
    </nav>
  </aside>
</template>

<script setup>
import { RouterLink } from 'vue-router'
</script>

<style scoped>
.sidebar {
  background: #ffffffcc;
  backdrop-filter: blur(10px);
}
.nav-item {
  padding: 10px 14px;
  border-radius: 10px;
  font-size: 15px;
  transition: 0.2s;
  color: #333;
}
.nav-item:hover {
  background: #f2f2f2;
}
.active {
  background: #e3e8ff;
  color: #2f3bcf;
  font-weight: 600;
}
</style>
