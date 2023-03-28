<script setup lang="ts">
defineProps<{
  sticky?: boolean;
}>();
</script>

<template>
  <div class="bg-neutral-900" :class="{ 'sticky top-0': sticky }">
    <div class="flex gap-4 justify-between px-4 py-3 text-white font-semibold">
      <slot />
    </div>
    <div class="border-b border-neutral-700"></div>
  </div>
</template>
