<script setup>
import List from '@/components/List/List.vue';

const lists = [
  {
    name: 'Tech Stack',
    items: [
      {
        name: 'Vue.js',
        icon: 'https://upload.wikimedia.org/wikipedia/commons/9/95/Vue.js_Logo_2.svg',
      },
      {
        name: 'React.js',
        icon: 'https://upload.wikimedia.org/wikipedia/commons/a/a7/React-icon.svg',
      },
      {
        name: 'Node.js',
        icon: 'https://upload.wikimedia.org/wikipedia/commons/d/d9/Node.js_logo.svg',
      },
      {
        name: 'Express.js',
        icon: 'https://upload.wikimedia.org/wikipedia/commons/6/64/Expressjs.png',
      },
      {
        name: 'MongoDB',
        icon: 'https://upload.wikimedia.org/wikipedia/commons/9/93/MongoDB_Logo.svg',
      },
    ],
  },
  {
    name: "Tools I'm using",
    items: [
      {
        name: 'VS Code',
        icon: 'https://upload.wikimedia.org/wikipedia/commons/9/9a/Visual_Studio_Code_1.35_icon.svg',
      },
      {
        name: 'Figma',
        icon: 'https://upload.wikimedia.org/wikipedia/commons/3/33/Figma-logo.svg',
      },
      {
        name: 'Git',
        icon: 'https://upload.wikimedia.org/wikipedia/commons/3/3f/Git_icon.svg',
      },
      {
        name: 'GitHub',
        icon: 'https://upload.wikimedia.org/wikipedia/commons/9/91/Octicons-mark-github.svg',
      },
      {
        name: 'Vite',
        icon: 'https://upload.wikimedia.org/wikipedia/commons/f/f1/Vitejs-logo.svg',
      },
    ],
  },
];
</script>

<template>
  <section class="flex h-full w-full flex-col justify-center gap-9 rounded-r-lg p-10">
    <List v-for="(list, idx) in lists" :key="idx" :list="list"></List>
    <span class="select-none text-[32px]">My Projects -></span>
  </section>
</template>
