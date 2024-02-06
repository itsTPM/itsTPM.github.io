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
    class="flex h-[58px] w-[58px] items-center justify-center rounded-lg border bg-[rgba(0,0,0,0.2)] transition hover:scale-110"
    target="_blank">
    <img :alt="item.title" :src="iconSrc" class="h-[32px] w-[32px] select-none" draggable="false" />
  </a>
</template>
