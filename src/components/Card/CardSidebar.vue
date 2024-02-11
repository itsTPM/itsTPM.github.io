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
    class="flex w-[256px] flex-col rounded-s-lg border-r sm:w-full sm:items-center sm:justify-between sm:rounded-none sm:border-b sm:pt-10">
    <div class="max-h-[256px] max-w-[256px] rounded-ss-lg">
      <img
        alt="Avatar"
        class="max-h-full max-w-full select-none rounded-ss-lg object-contain sm:rounded-lg"
        draggable="false"
        src="https://avatars.githubusercontent.com/u/26815728" />
    </div>
    <div class="flex flex-grow flex-col items-center justify-between rounded-es-lg p-6 sm:gap-6">
      <div class="flex flex-col items-center justify-center">
        <span class="font-mono text-[40px] leading-10">itsTPM</span>
        <span class="font-ubuntu text-[16px] font-light">pseudo-frontend™</span>
      </div>
      <div class="grid w-max grid-cols-3 grid-rows-1 gap-4">
        <CardSidebarButton v-for="item in links" :item="item"></CardSidebarButton>
      </div>
    </div>
  </section>
</template>
