<script setup lang="ts">
defineProps<{
  to?: string;
}>();
</script>

<template>
  <li>
    <NuxtLink
      :to="to"
      class="px-2 py-1.5 rounded-md text-neutral-400 hover:bg-neutral-800 text-sm block w-full text-left"
    >
      <slot />
    </NuxtLink>
  </li>
</template>
