<script setup lang="ts">
//
</script>

<template>
  <header
    class="flex items-center fixed w-full top-0 border-b border-neutral-800 px-3 py-2 z-10 bg-neutral-900"
  >
    <div class="flex-1 flex justify-center">
      <input
        type="text"
        placeholder="Search"
        class="px-4 py-1.5 rounded-lg w-6/12 bg-neutral-800"
      />
    </div>
    <div>
      <div class="bg-neutral-700 w-8 h-8 rounded-lg" />
    </div>
  </header>
  <div class="flex bg-neutral-900 h-[calc(100vh-53px)] fixed top-[53px] w-full">
    <WorkspaceList />
    <Navigation />
    <div class="flex-1 relative overflow-y-auto">
      <slot />
    </div>
  </div>
  <!-- banner -->
</template>
