<script setup lang="ts">
import { ref } from 'vue'
import {Link} from "@inertiajs/vue3";


const isOpen = ref(false)

const closeMenu = () => {
    isOpen.value = false
}
</script>


<style scoped>
/* 🌟 Transitions */
.fade-enter-active,
.fade-leave-active {
    transition: opacity 0.3s;
}
.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}

.scale-enter-active,
.scale-leave-active {
    transition: transform 0.3s ease, opacity 0.3s ease;
}
.scale-enter-from,
.scale-leave-to {
    transform: scale(0.8);
    opacity: 0;
}
</style>

<template>
    <div class="w-full theme-nav-color flex rounded-full ">
        <div class="h-full w-full flex items-center justify-between px-8 py-2">
            <Link :href="route('home')" class="text-white text-[28px] flex">
                সু-শাসন আন্দোলন
            </Link>
            <div class="text-white text-[28px] flex hidden lg:block">
                <Link :href="route('blog')" class="ml-12">ব্লগ</Link>
                <Link :href="route('publishing')" class="ml-12">প্রকাশনী</Link>
                <Link :href="route('contact')" class="ml-12">যোগাযোগ</Link>
            </div>
            <svg @click="isOpen = true" class="h-8 text-white font-bold lg:hidden" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>

        </div>
        <transition name="fade">
            <div
                v-if="isOpen"
                @click.self="closeMenu"
                class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-40"
            >
                <!-- 🌟 Centered Menu -->
                <transition name="scale">
                    <div
                        v-if="isOpen"
                        class="bg-white rounded-2xl p-6 w-80 shadow-xl z-50"
                    >
                        <h2 class="text-xl font-bold mb-4 text-center">Menu</h2>

                        <ul class="space-y-2 text-center">
                            <li><Link :href="route('home')" class="block hover:text-blue-600 text-2xl">হোম</Link></li>
                            <li><Link :href="route('blog')" class="block hover:text-blue-600 text-2xl">ব্লগ</Link></li>
                            <li><Link :href="route('publishing')" class="block hover:text-blue-600 text-2xl">প্রকাশনী</Link></li>
                            <li><Link :href="route('contact')" class="block hover:text-blue-600 text-2xl">যোগাযোগ</Link></li>
                        </ul>

                        <button
                            @click="closeMenu"
                            class="mt-6 w-full bg-gray-200 hover:bg-gray-300 text-gray-800 py-2 rounded-lg"
                        >
                            Close
                        </button>
                    </div>
                </transition>
            </div>
        </transition>
    </div>
</template>

<style scoped>

</style>
