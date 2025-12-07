<template>
  <div class="layout">
    <!-- LEFT SIDEBAR -->
    <aside class="left">
      <Sidebar />
    </aside>

    <!-- MAIN FEED -->
    <main class="center">
      <RouterView />
    </main>

    <!-- RIGHT PROFILE CARD -->
    <aside class="right">
      <CrewCard />
    </aside>
  </div>
</template>

<script setup>
import CrewCard from '@/components/ui/CrewCard.vue';
import Sidebar from '@/components/ui/Sidebar.vue';
import { RouterView } from 'vue-router'
</script>

<style scoped>
.layout {
  display: grid;
  grid-template-columns: 260px 1fr 350px; /* EXACT Twitter layout proportions */
  width: 100vw;
  height: 100vh;
  overflow: hidden;
}

/* LEFT: fixed menu */
.left {
  border-right: 1px solid #e5e5e5;
  background: #fff;
  height: 100%;
  padding: 20px 0;
}

/* CENTER: main feed (no max width, no gap!) */
.center {
  height: 100%;
  overflow-y: auto;
  padding-bottom: 40px;
}

/* RIGHT: profile + widgets */
.right {
  border-left: 1px solid #e5e5e5;
  background: #fafafa;
  height: 100%;
  overflow-y: auto;
  padding: 20px;
}
</style>
