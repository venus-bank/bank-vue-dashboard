<script setup lang="ts">
import { RouterView } from 'vue-router';

import Sidebar from '@/components/Sidebar.vue';
import Navbar from '@/components/Navbar.vue';
</script>

<template>
  <div class="flex">
    <Sidebar class="w-72 min-w-[16rem]" />

    <!-- main content -->
    <main class="overflow-hidden w-full">
      <Navbar />

      <div class="px-4 bg-gray-100 py-4 min-h-screen">
        <RouterView />
      </div>
    </main>
  </div>
</template>

<style>
/* import font awesome style */
@import '@/assets/font.min.css';

/* editor custom style */
.ck-editor__editable_inline {
  min-height: 10rem;
  max-height: 15rem;
  overflow-y: scroll;
}

.dashboard {
  grid-template-columns: 16rem 1fr;
}
</style>
