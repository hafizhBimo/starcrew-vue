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
  grid-template-columns: 260px minmax(400px, 600px) 350px;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  justify-content: center;
}

/* LEFT: fixed menu */
.left {
  border-right: 1px solid #e5e5e5;
  background: #fff;
  height: 100%;
  padding: 20px 0;
  max-width: 260px;
  justify-self: end;
}

/* CENTER: main feed */
.center {
  height: 100%;
  overflow-y: auto;
  padding-bottom: 40px;
  max-width: 600px;
  width: 100%;
  margin: 0 auto;
}

/* RIGHT: widgets */
.right {
  border-left: 1px solid #e5e5e5;
  background: #fafafa;
  height: 100%;
  overflow-y: auto;
  padding: 20px;
  max-width: 350px;
}

/* ------------------------------------------
   TABLET — hide RIGHT sidebar
------------------------------------------- */
@media (max-width: 1100px) {
  .layout {
    grid-template-columns: 260px minmax(300px, 1fr);
  }

  .right {
    display: none;
  }
}

/* ------------------------------------------
   MOBILE — hide BOTH sidebars
------------------------------------------- */
@media (max-width: 900px) {
  .layout {
    grid-template-columns: 1fr;
  }

  .left,
  .right {
    display: none;
  }

  .center {
    max-width: 600px;
    width: 100%;
    margin: 0 auto;
    padding: 16px;
  }
}
</style>
