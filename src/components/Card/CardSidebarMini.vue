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
    class="flex min-h-[30rem] w-20 flex-col rounded-s-lg border-r sm:w-full sm:items-center sm:justify-between sm:rounded-none sm:border-0 sm:border-b">
    <div class="aspect-square rounded-ss-lg">
      <img
        alt="Avatar"
        class="aspect-square w-64 select-none rounded-ss-lg object-contain sm:min-w-32 sm:rounded-lg"
        draggable="false"
        src="https://avatars.githubusercontent.com/u/26815728" />
    </div>
    <div
      class="flex w-full flex-grow flex-col items-center justify-between rounded-es-lg p-2 pb-4 pt-8 xs:px-0 sm:gap-6">
      <div class="w-full rotate-90 text-center">
        <h1 class="font-mono text-2xl leading-10">itsTPM</h1>
      </div>
      <div class="flex w-fit flex-col items-center gap-4">
        <CardSidebarButton v-for="item in links" :item="item" class="h-full w-full max-w-14 p-2"></CardSidebarButton>
      </div>
    </div>
  </section>
</template>
