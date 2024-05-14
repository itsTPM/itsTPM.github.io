<script setup>
import Card from '@/components/Card/Card.vue';
import CardContent from '@/components/Card/CardContent.vue';
import CardSidebarMini from '@/components/Card/CardSidebarMini.vue';
import CardSidebar from '@/components/Card/CardSidebar.vue';
import List from '@/components/List/List.vue';
import Button from '@/components/ui/button/Button.vue';
import {
  Dialog,
  DialogContent,
  DialogDescription,
  DialogFooter,
  DialogHeader,
  DialogTitle,
  DialogTrigger,
} from '@/components/ui/dialog';
import data from '@/data.json';

const { links, projects } = data;

const getIconSrc = (path) => {
  return new URL(`/src/assets/icons/${path}`, import.meta.url).href;
};

const formatText = (text) => {
  // *test* -> <i>test</i>
  // **test** -> <b>test</b>

  return text.replace(/\*{2}(.+?)\*{2}/g, '<b>$1</b>').replace(/\*(.+?)\*/g, '<i>$1</i>');
};
</script>

<template>
  <Card>
    <CardSidebarMini :links="links" class="sm:hidden"></CardSidebarMini>
    <CardSidebar :links="links" class="hidden sm:flex"></CardSidebar>
    <CardContent>
      <RouterLink
        to="/"
        class="cursor-pointer select-none text-3xl before:inline-block before:transition before:content-['<-'] motion-safe:hover:before:-translate-x-2">
        Back
      </RouterLink>

      <List :listName="projects.name">
        <ul class="grid grid-cols-2 gap-5 sm:grid-cols-1">
          <li
            v-for="(item, idx) in projects.items"
            :key="idx"
            class="flex max-w-[25rem] select-none items-center justify-center rounded-lg border bg-black/20 transition motion-safe:hover:scale-105 xs:w-full sm:flex-col">
            <div class="flex h-full items-center justify-center border-r px-6 py-2 sm:w-full sm:border-b sm:border-r-0">
              <img
                :src="item.image"
                class="aspect-square h-20 w-20 object-contain"
                draggable="false"
                :alt="`${item.name} Logo`" />
            </div>

            <div class="flex max-w-full flex-col gap-2 p-3">
              <div>
                <p class="text-xl">{{ item.name }}</p>
                <p class="text-sm text-muted-foreground">{{ item.desc }}</p>
              </div>

              <div class="flex items-center gap-3">
                <template v-for="button in item.buttons">
                  <Dialog>
                    <DialogTrigger as-child>
                      <Button variant="outline" size="sm" v-if="button.type === 'text'">{{ button.title }}</Button>
                    </DialogTrigger>
                    <DialogContent>
                      <DialogHeader>
                        <DialogTitle>{{ button.dialog.title }}</DialogTitle>
                      </DialogHeader>
                      <DialogDescription v-html="formatText(button.dialog.description)"></DialogDescription>
                    </DialogContent>
                  </Dialog>

                  <Button
                    variant="ghost"
                    size="sm"
                    v-if="button.type === 'icon'"
                    class="aspect-square p-1"
                    :title="button.title"
                    :aria-label="`Link to ${button.title}`"
                    as="a"
                    :href="button.href">
                    <img
                      :src="getIconSrc(button.icon)"
                      class="max-h-full max-w-full object-contain"
                      draggable="false"
                      :alt="`${item.name} Logo`" />
                  </Button>
                </template>
              </div>
            </div>
          </li>
        </ul>
      </List>
    </CardContent>
  </Card>
</template>
