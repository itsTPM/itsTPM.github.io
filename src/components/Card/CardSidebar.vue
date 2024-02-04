<script setup>
import CardSidebarButton from '@/components/Card/CardSidebarButton.vue';

const links = [
  {
    title: 'Telegram',
    icon: 'Telegram-Logo.svg',
    url: 'https://t.me/itsTPM',
  },
  {
    title: 'GitHub',
    icon: 'GitHub-Logo.svg',
    url: 'https://github.com/itsTPM',
  },
  {
    title: 'Spotify',
    icon: 'Spotify-Logo.svg',
    url: 'https://open.spotify.com/user/lyoshabt',
  },
];
</script>

<template>
  <section class="flex h-full w-[256px] flex-col rounded-s-lg bg-red-400">
    <div class="h-[256px] w-[256px] rounded-ss-lg bg-blue-400">
      <!-- Avatar -->
    </div>
    <div class="flex flex-grow flex-col items-center justify-between rounded-es-lg bg-green-400 p-6">
      <div class="flex flex-col items-center justify-center">
        <span class="font-mono text-[40px] leading-10">itsTPM</span>
        <span class="font-ubuntu text-[16px] font-light">pseudo-frontend™</span>
      </div>
      <div class="grid grid-cols-3 grid-rows-1 gap-4">
        <CardSidebarButton v-for="item in links" :item="item"></CardSidebarButton>
      </div>
    </div>
  </section>
</template>
