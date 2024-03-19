<script setup>
const props = defineProps({
  item: {
    type: Object,
    required: true,
  },
});

const iconSrc = new URL(`/src/assets/icons/${props.item.icon}`, import.meta.url).href;
</script>

<template>
  <div
    class="flex select-none flex-col items-center justify-center rounded-lg border bg-black/20 p-3 transition motion-safe:hover:scale-110">
    <img :src="iconSrc" class="h-16 w-16 object-contain" draggable="false" :alt="`${item.name} Logo`" />
    <span>{{ item.name }}</span>
  </div>
</template>
