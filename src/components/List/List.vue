<script setup>
import ListItem from '@/components/List/ListItem.vue';

const props = defineProps({
  list: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="flex flex-col gap-9">
    <span class="text-2xl">{{ list.name }}</span>
    <div class="grid grid-cols-5 grid-rows-1 gap-[20px]">
      <ListItem v-for="(item, idx) in list.items" :key="idx" :item="item"></ListItem>
    </div>
  </div>
</template>
