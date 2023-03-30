<script setup lang="ts">
const menus = [
  {
    title: 'Threads',
    to: '/threads',
    prefixIcon: 'ic:round-comment',
  },
  {
    title: 'Direct Messages',
    to: '/messages',
    prefixIcon: 'ic:round-chat-bubble-outline',
  },
  {
    title: 'Mentions and Reactions',
    to: '/mentions',
    prefixIcon: 'ri:at-line',
  },
  {
    title: 'Drafts and sent',
    to: '/drafts',
    prefixIcon: 'ri:draft-line',
  },
  {
    title: 'Saved items',
    to: '/saved',
    prefixIcon: 'ri:bookmark-line',
  },
  {
    title: 'Slack Connect',
    to: '/connect',
    prefixIcon: 'ic:round-people-outline',
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
      <button
        aria-label="Add"
        class="text-sm text-neutral-800 bg-white hover:bg-neutral-200 rounded-full w-7 h-7 grid place-items-center"
      >
        <Icon name="ri:add-line" size="20px" />
      </button>
    </AppBar>
    <ScrollArea class="pb-20">
      <List>
        <ListItem
          v-for="{ title, ...menu } in menus"
          :key="title"
          v-bind="menu"
        >
          {{ title }}
        </ListItem>
        <ListItem prefix-icon="ri:more-2-line"> More </ListItem>
      </List>
      <Separator />
      <List>
        <ListHeader>Channels</ListHeader>
        <ListItem
          v-for="channel in channels"
          :key="channel.name"
          :to="`/channels/${channel.id}`"
          prefix-icon="ri:hashtag"
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
          prefix-icon="ri:user-fill"
        >
          {{ message.user }}
        </ListItem>
      </List>
      <Separator />
      <List>
        <ListHeader>Apps</ListHeader>
        <ListItem
          v-for="app in apps"
          :key="app.id"
          :to="`/apps/${app.id}`"
          prefix-icon="ri:apps-fill"
        >
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
