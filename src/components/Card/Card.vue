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
  <div
    class="flex max-w-full rounded-lg border bg-[#0e0e0e] bg-gradient-to-br from-sky-100/5 to-sky-900/5 bg-cover sm:flex-col sm:bg-none">
    <CardSidebar :links="links"></CardSidebar>
    <CardContent :lists="lists"></CardContent>
  </div>
</template>
