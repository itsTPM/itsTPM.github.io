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
  <a
    :href="item.url"
    class="flex items-center justify-center rounded-lg border bg-black/20 p-3 transition motion-safe:hover:scale-110"
    target="_blank">
    <img :alt="item.title" :src="iconSrc" class="h-8 w-8 select-none" draggable="false" />
  </a>
</template>
