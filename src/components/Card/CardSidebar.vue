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
    class="flex w-64 flex-col rounded-s-lg border-r sm:w-full sm:items-center sm:justify-between sm:rounded-none sm:border-b sm:pt-10">
    <div class="aspect-square max-h-64 max-w-64 rounded-ss-lg">
      <img
        alt="Avatar"
        class="aspect-square max-h-full max-w-full select-none rounded-ss-lg object-contain sm:rounded-lg"
        draggable="false"
        src="https://avatars.githubusercontent.com/u/26815728" />
    </div>
    <div class="flex flex-grow flex-col items-center justify-between rounded-es-lg p-6 sm:gap-6">
      <div class="text-center">
        <div class="font-mono text-[40px] leading-10">itsTPM</div>
        <div class="font-ubuntu font-light">pseudo-frontend™</div>
      </div>
      <div class="grid w-max grid-cols-3 grid-rows-1 gap-4">
        <CardSidebarButton v-for="item in links" :item="item"></CardSidebarButton>
      </div>
    </div>
  </section>
</template>
