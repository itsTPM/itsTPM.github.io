<script setup>
const props = defineProps({
  item: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div
    class="flex select-none flex-col items-center justify-center rounded-lg border bg-[rgba(0,0,0,0.2)] p-3 transition hover:scale-110">
    <img :src="item.icon" alt="" class="h-[64px] w-[64px] object-contain" />
    <span>{{ item.name }}</span>
  </div>
</template>
