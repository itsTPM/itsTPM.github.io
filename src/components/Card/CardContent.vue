<script setup>
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
  <section class="flex h-full w-full flex-col justify-center gap-9 rounded-r-lg bg-purple-300 p-10">
    <div v-for="(list, idx) in lists" :key="idx" class="flex flex-col gap-9">
      <span class="text-2xl">{{ list.name }}</span>
      <div class="grid grid-cols-5 grid-rows-1 gap-[20px]">
        <div
          v-for="(item, idx) in list.items"
          :key="idx"
          class="flex flex-col items-center justify-center rounded-lg border border-[#222] bg-orange-400 p-3">
          <img :src="item.icon" alt="" class="h-[64px] w-[64px] object-contain" />
          <span>{{ item.name }}</span>
        </div>
      </div>
    </div>

    <span class="text-[32px]">My Projects -></span>
  </section>
</template>
