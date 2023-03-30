<script setup lang="ts">
withDefaults(
  defineProps<{
    to?: string;
    prefixIcon?: string;
    prefixIconSize?: string;
    prefixIconClass?: string;
    suffixIcon?: string;
    suffixIconSize?: string;
    suffixIconClass?: string;
  }>(),
  {
    prefixIconSize: '20px',
    suffixIconSize: '20px',
  }
);
</script>

<template>
  <li>
    <NuxtLink
      :to="to"
      class="px-2 py-1.5 rounded-md text-neutral-400 hover:bg-neutral-800 text-sm flex items-center w-full text-left gap-3"
    >
      <slot name="prefix">
        <Icon
          v-if="prefixIcon"
          :name="prefixIcon"
          :size="prefixIconSize"
          :class="prefixIconClass"
        />
      </slot>
      <slot />
      <slot name="suffix">
        <Icon
          v-if="suffixIcon"
          :name="suffixIcon"
          :size="suffixIconSize"
          :class="suffixIconClass"
        />
      </slot>
    </NuxtLink>
  </li>
</template>
