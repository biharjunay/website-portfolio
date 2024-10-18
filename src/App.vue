<template>
  <div class="flex h-screen text-white">
    <div class="w-2/12 h-full">
      <SidebarItem />
    </div>
    <div class="w-10/12 pt-5 px-3">
      <RouterView />
    </div>
  </div>
</template>

<script lang="ts">
import SidebarItem from "@/components/SidebarItem.vue";
export default {
  components: {
    SidebarItem
  }
}
</script>