<script setup>
import List from '@/components/List/List.vue';
import { HoverCard, HoverCardContent, HoverCardTrigger } from '@/components/ui/hover-card';

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
  <section class="flex h-full w-full flex-col items-baseline justify-center gap-9 rounded-r-lg px-10 py-12">
    <List v-for="(list, idx) in lists" :key="idx" :list="list"></List>

    <HoverCard close-delay="200" openDelay="0">
      <HoverCardTrigger>
        <span
          class="cursor-pointer select-none text-[32px] after:inline-block after:animate-bounce-to-right after:transition after:content-['->'] hover:after:translate-x-2">
          My Projects
        </span>
      </HoverCardTrigger>

      <HoverCardContent>
        <div class="font-bold">This page isn't ready yet :P</div>
        <div>But one day it will be available...</div>
      </HoverCardContent>
    </HoverCard>
  </section>
</template>
