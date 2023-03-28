<script setup lang="ts"></script>

<template>
  <div class="flex flex-col relative">
    <!-- title -->
    <AppBar sticky>Welcome</AppBar>
    <!-- messages -->
    <ScrollArea class="space-y-2">
      <div v-for="i in 20" class="flex px-4 py-2 gap-4 hover:bg-neutral-800">
        <div class="w-10 h-10 bg-neutral-500 rounded-md shrink-0"></div>
        <div class="flex-1">
          <div class="flex items-center gap-2">
            <button class="font-semibold text-neutral-300 text-sm">
              John Doe
            </button>
            <span class="text-xs text-neutral-500">10.53 PM</span>
          </div>
          <article class="text-sm text-neutral-400">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo quaerat
            cum, nemo sunt, id reprehenderit at iste fuga consectetur omnis
            minima repudiandae odit a ut eveniet neque sapiente voluptatem est?
          </article>
        </div>
      </div>
    </ScrollArea>
    <!-- input -->
    <div class="flex gap-4 px-4 py-4 bg-neutral-900 sticky bottom-0">
      <textarea
        class="w-full bg-neutral-800 text-neutral-200 rounded-md px-4 py-2 text-sm"
        placeholder="Message #general"
      ></textarea>
    </div>
  </div>
</template>
