<script setup lang="ts">
const menus = [
  {
    title: 'Threads',
    to: '/threads',
  },
  {
    title: 'Direct Messages',
    to: '/messages',
  },
  {
    title: 'Mentions and Reactions',
    to: '/mentions',
  },
  {
    title: 'Drafts and sent',
    to: '/drafts',
  },
  {
    title: 'Saved items',
    to: '/saved',
  },
  {
    title: 'Slack Connect',
    to: '/connect',
  },
  {
    title: 'Saved items',
    to: '/saved',
  },
];

const channels = [
  {
    id: 1,
    name: 'Channel 1',
  },
  {
    id: 2,
    name: 'Channel 2',
  },
  {
    id: 3,
    name: 'Channel 3',
  },
  {
    id: 4,
    name: 'Channel 4',
  },
  {
    id: 5,
    name: 'Channel 5',
  },
  {
    id: 6,
    name: 'Channel 6',
  },
  {
    id: 7,
    name: 'Channel 7',
  },
  {
    id: 8,
    name: 'Channel 8',
  },
  {
    id: 9,
    name: 'Channel 9',
  },
  {
    id: 10,
    name: 'Channel 10',
  },
  {
    id: 11,
    name: 'Channel 11',
  },
  {
    id: 12,
    name: 'Channel 12',
  },
  {
    id: 13,
    name: 'Channel 13',
  },
  {
    id: 14,
    name: 'Channel 14',
  },
  {
    id: 15,
    name: 'Channel 15',
  },
  {
    id: 16,
    name: 'Channel 16',
  },
  {
    id: 17,
    name: 'Channel 17',
  },
  {
    id: 18,
    name: 'Channel 18',
  },
  {
    id: 19,
    name: 'Channel 19',
  },
  {
    id: 20,
    name: 'Channel 20',
  },
  {
    id: 21,
    name: 'Channel 21',
  },
  {
    id: 22,
    name: 'Channel 22',
  },
  {
    id: 23,
    name: 'Channel 23',
  },
  {
    id: 24,
    name: 'Channel 24',
  },
  {
    id: 25,
    name: 'Channel 25',
  },
  {
    id: 26,
    name: 'Channel 26',
  },
  {
    id: 27,
    name: 'Channel 27',
  },
  {
    id: 28,
    name: 'Channel 28',
  },
  {
    id: 29,
    name: 'Channel 29',
  },
  {
    id: 30,
    name: 'Channel 30',
  },
  {
    id: 31,
    name: 'Channel 31',
  },
];

const messages = [
  {
    id: 1,
    user: 'User 1',
  },
  {
    id: 2,
    user: 'User 2',
  },
  {
    id: 3,
    user: 'User 3',
  },
];

const apps = [
  {
    id: 1,
    name: 'App 1',
  },
  {
    id: 2,
    name: 'App 2',
  },
  {
    id: 3,
    name: 'App 3',
  },
];
</script>

<template>
  <div
    class="flex flex-col border-r border-neutral-700 w-3/12 xl:w-2/12 relative"
  >
    <AppBar>
      <NuxtLink to="/" class="font-semibold text-white">
        Workspace Name
      </NuxtLink>
      <button class="text-sm text-neutral-200">Add</button>
    </AppBar>
    <ScrollArea class="pb-20">
      <List>
        <ListItem v-for="menu in menus" :key="menu.title" :to="menu.to">
          {{ menu.title }}
        </ListItem>
        <li>
          <button
            class="px-2 py-1.5 rounded-md text-neutral-400 hover:bg-neutral-800 text-sm block text-left"
          >
            More
          </button>
        </li>
      </List>
      <Separator />
      <List>
        <ListHeader>Channels</ListHeader>
        <ListItem
          v-for="channel in channels"
          :key="channel.name"
          :to="`/channels/${channel.id}`"
        >
          {{ channel.name }}
        </ListItem>
      </List>
      <Separator />
      <List>
        <ListHeader> Direct Messages </ListHeader>
        <ListItem
          v-for="message in messages"
          :key="message.id"
          :to="`/messages/${message.id}`"
        >
          {{ message.user }}
        </ListItem>
      </List>
      <Separator />
      <List>
        <ListHeader>Apps</ListHeader>
        <ListItem v-for="app in apps" :key="app.id" :to="`/apps/${app.id}`">
          {{ app.name }}
        </ListItem>
      </List>
    </ScrollArea>
    <!-- huddle -->
    <div class="absolute bottom-0 left-0 right-0 bg-neutral-900">
      <Separator />
      <div class="flex items-center py-3 px-3">
        <div class="w-3 h-3 rounded-full bg-green-500 mr-2"></div>
        <span class="text-sm">Huddle</span>
      </div>
    </div>
  </div>
</template>
