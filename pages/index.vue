<script setup lang="ts">
definePageMeta({
  colorMode: 'dark',
})

import {
  Drawer,
  DrawerClose,
  DrawerContent,
  DrawerDescription,
  DrawerFooter,
  DrawerHeader,
  DrawerTitle,
  DrawerTrigger,
} from '@/components/ui/drawer'
</script>

<template>
  <Map />
  <Drawer>
    <DrawerTrigger>
      <Button class="dark:color-border" variant="outline">
        Open Drawer <Icon name="mdi:github" />
      </Button>
    </DrawerTrigger>
    <DrawerContent>
      <DrawerHeader>
        <DrawerTitle>Are you absolutely sure?</DrawerTitle>
        <DrawerDescription>This action cannot be undone.</DrawerDescription>
      </DrawerHeader>
      <div class="max-w-[400px] px-6 m-auto">
        <Label for="picture">Picture</Label>
        <Input id="picture" type="file" />
      </div>
      <DrawerFooter>
        <Button>Submit</Button>
        <DrawerClose>
          <Button variant="outline">
            Cancel
          </Button>
        </DrawerClose>
      </DrawerFooter>
    </DrawerContent>
  </Drawer>
</template>