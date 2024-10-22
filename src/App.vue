<template>
  <div class="flex h-screen text-white bg-gradient-to-br from-gray-800 to-black">
    <div class="w-[10%] h-full">
      <SidebarItem />
    </div>
    <div class="w-[90%] px-3 py-5 h-full overflow-x-auto">
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