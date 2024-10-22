<template>
    <div class="flex flex-col items-center h-full border-r border-r-zinc-700">
        <img class="w-20 m-5" src="@/assets/images/logo.png" alt="image">
        <div class="flex flex-col justify-between h-full w-full text-white py-5">
            <RouterLink :to="`/${item.name}`"
                class="flex flex-col justify-center text-center relative py-3 cursor-pointer hover:text-blue-600 transition-all"
                :class="{ 'text-blue-400': currentRoute === item.name }" v-for="(item, index) in sidebarItem"
                :key="index">
                <i :class="item.icon + ' text-4xl'"></i>
                <span class="capitalize">{{ item.name }}</span>
                <div v-if="currentRoute === item.name"
                    class="absolute w-1 h-full bg-blue-400 rounded-full right-0 top-1/2 -translate-y-1/2"></div>
            </RouterLink>
        </div>
    </div>
</template>
<script lang="ts">
export default {
    data() {
        return {
            sidebarItem: [
                { icon: 'fas fa-house', name: 'home' },
                { icon: 'fas fa-user', name: 'about' },
                { icon: 'fas fa-briefcase', name: 'portfolio' },
                { icon: 'fas fa-phone', name: 'contact' },
                { icon: 'fas fa-ellipsis-h', name: 'other' },
            ] satisfies { name: string, icon: string }[]
        }
    },
    computed: {
        currentRoute() {
            return this.$route.name
        }
    }
}
</script>