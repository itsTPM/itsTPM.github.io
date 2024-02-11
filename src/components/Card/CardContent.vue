<script setup>
import List from '@/components/List/List.vue';
import { HoverCard, HoverCardContent, HoverCardTrigger } from '@/components/ui/hover-card';

const props = defineProps({
  lists: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <section class="flex h-full w-full flex-col items-baseline justify-center gap-9 rounded-r-lg px-10 py-12">
    <List v-for="(list, idx) in lists" :key="idx" :list="list"></List>

    <HoverCard close-delay="200" openDelay="0">
      <HoverCardTrigger>
        <span
          class="cursor-pointer select-none text-[32px] after:inline-block after:transition after:content-['->'] motion-safe:after:animate-bounce-to-right motion-safe:hover:after:translate-x-2">
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
