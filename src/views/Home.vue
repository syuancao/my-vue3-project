<template>
  <div class="home">
    <ItemsListComponent :items="items" />
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive } from "vue";
import ItemsListComponent from "@/components/items/itemsList.component.vue";
import { ItemInterface } from "@/models/items/Item.interface";

export default defineComponent({
  name: "Home",
  components: {
    ItemsListComponent,
  },
  setup() {
    const items: ItemInterface[] = reactive([
      {
        id: 1,
        name: "Item 1",
        selected: false,
      },
      {
        id: 2,
        name: "Item 2",
        selected: false,
      },
      {
        id: 3,
        name: "Item 3",
        selected: false,
      },
    ]);
    return {
      items,
    };
  },
});
</script>>
