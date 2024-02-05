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
  <button class="flex h-[58px] w-[58px] items-center justify-center rounded-lg transition hover:scale-110">
    <img :alt="item.title" :src="iconSrc" class="h-[32px] w-[32px]" />
  </button>
</template>
