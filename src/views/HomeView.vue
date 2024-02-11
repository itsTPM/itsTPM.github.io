<script setup>
import Card from '@/components/Card/Card.vue';
import data from '@/data.json';

const { links, lists } = data;
</script>

<template>
  <Card :links="links" :lists="lists"></Card>
</template>
