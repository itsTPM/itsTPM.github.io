<script setup>
import CardSidebarButton from '@/components/Card/CardSidebarButton.vue';

const props = defineProps({
  links: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <section
    class="flex w-64 flex-col rounded-s-lg border-r sm:w-full sm:items-center sm:justify-between sm:rounded-none sm:border-0 sm:border-b sm:px-10 sm:pt-10">
    <div class="aspect-square rounded-ss-lg">
      <img
        alt="Avatar"
        class="aspect-square w-64 select-none rounded-ss-lg object-contain sm:min-w-32 sm:rounded-lg"
        draggable="false"
        src="https://avatars.githubusercontent.com/u/26815728" />
    </div>
    <div class="flex w-full flex-grow flex-col items-center justify-between rounded-es-lg p-6 xs:px-0 sm:gap-6">
      <div class="text-center">
        <h1 class="font-mono text-[2.5rem] leading-10">itsTPM</h1>
        <h2 class="font-ubuntu font-light">pseudo-frontend™</h2>
      </div>
      <div class="grid w-max max-w-full grid-cols-3 grid-rows-1 gap-4">
        <CardSidebarButton v-for="item in links" :item="item"></CardSidebarButton>
      </div>
    </div>
  </section>
</template>
