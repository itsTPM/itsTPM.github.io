<script setup>
import List from '@/components/List/List.vue';

const lists = [
  {
    name: 'Tech Stack',
    items: [
      {
        name: 'HTML',
        icon: 'HTML-Logo.svg',
      },
      {
        name: 'CSS',
        icon: 'CSS-Logo.svg',
      },
      {
        name: 'TailwindCSS',
        icon: 'TailwindCSS-Logo.svg',
      },
      {
        name: 'JavaScript',
        icon: 'JavaScript-Logo.svg',
      },
      {
        name: 'Vue.js',
        icon: 'Vue.js-Logo.svg',
      },
    ],
  },
  {
    name: "Tools I'm using",
    items: [
      {
        name: 'VS Code',
        icon: 'VSCode-Logo.svg',
      },
      {
        name: 'WebStorm',
        icon: 'WebStorm-Logo.svg',
      },
      {
        name: 'Git',
        icon: 'Git-Logo.svg',
      },
      {
        name: 'Vite',
        icon: 'Vite-Logo.svg',
      },
      {
        name: 'Figma',
        icon: 'Figma-Logo.svg',
      },
    ],
  },
];
</script>

<template>
  <section class="flex h-full w-full flex-col items-baseline justify-center gap-9 rounded-r-lg p-10">
    <List v-for="(list, idx) in lists" :key="idx" :list="list"></List>
    <span class="select-none text-[32px]">My Projects -></span>
  </section>
</template>
