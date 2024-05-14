<script setup>
import Card from '@/components/Card/Card.vue';
import CardContent from '@/components/Card/CardContent.vue';
import CardSidebar from '@/components/Card/CardSidebar.vue';
import List from '@/components/List/List.vue';
import ListItem from '@/components/List/ListItem.vue';

import data from '@/data.json';

const { links, lists } = data;
</script>

<template>
  <Card>
    <CardSidebar :links="links"></CardSidebar>
    <CardContent>
      <List v-for="(list, idx) in lists" :key="idx" :listName="list.name">
        <ul class="grid grid-cols-5 grid-rows-1 gap-5 xs:!grid-cols-1 sm:grid-cols-2 md:grid-cols-3">
          <ListItem
            v-for="(item, idx) in list.items"
            :key="idx"
            :item="item"
            class="h-[7.1875rem] w-[7.3125rem]"></ListItem></ul
      ></List>

      <RouterLink
        to="/projects"
        class="cursor-pointer select-none text-3xl after:inline-block after:transition after:content-['->'] motion-safe:after:animate-bounce-to-right motion-safe:hover:after:translate-x-2">
        My Projects
      </RouterLink></CardContent
    >
  </Card>
</template>
