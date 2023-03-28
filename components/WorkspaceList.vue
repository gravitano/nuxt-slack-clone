<script setup lang="ts">
const workspaces = [
  {
    id: 1,
    name: 'Workspace 1',
    image: 'https://i.pravatar.cc/150?img=1',
  },
  {
    id: 2,
    name: 'Workspace 2',
    image: 'https://i.pravatar.cc/150?img=2',
  },
  {
    id: 3,
    name: 'Workspace 3',
    image: 'https://i.pravatar.cc/150?img=3',
  },
];

const active = ref(1);
</script>

<template>
  <div class="px-3 py-3 border-r min-h-screen border-neutral-700 relative">
    <ul class="space-y-4">
      <li
        v-for="workspace in workspaces"
        :key="workspace.name"
        class="group relative"
      >
        <button @click="active = workspace.id">
          <img
            :src="workspace.image"
            :alt="workspace.name"
            class="w-10 h-10 rounded-lg"
            :class="{
              'ring-4 ring-white': active === workspace.id,
            }"
          />
          <div
            class="absolute z-10 hidden group-hover:block group-focus-within:block right text-sm bg-black text-white px-3 py-2 rounded-lg w-auto left-12 top-1 min-w-max"
          >
            {{ workspace.name }}
          </div>
        </button>
      </li>
    </ul>
  </div>
</template>
