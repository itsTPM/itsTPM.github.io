<script setup>
import CardSidebar from '@/components/Card/CardSidebar.vue';
import CardContent from '@/components/Card/CardContent.vue';

const props = defineProps({
  lists: {
    type: Array,
    required: true,
  },
  links: {
    type: Array,
    required: true,
  },
});
</script>

<template>
  <div class="flex rounded-lg border bg-[#0e0e0e] bg-card-avatar bg-cover sm:m-5 sm:flex-col">
    <CardSidebar :links="links"></CardSidebar>
    <CardContent :lists="lists"></CardContent>
  </div>
</template>
