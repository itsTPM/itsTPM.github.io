<script setup>
const props = defineProps({
  listName: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="flex w-full flex-col gap-9">
    <p class="text-2xl">{{ listName }}</p>
    <slot></slot>
  </div>
</template>
