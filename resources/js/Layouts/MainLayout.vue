<script setup lang="ts">

import Header from "@/Components/Home/Header.vue";
</script>

<template>
    <div class="theme-color-background pt-8 relative min-h-screen">
        <div class="h-full w-full">
            <div class="px-4 lg:px-16">
                <Header></Header>
                <slot/>
            </div>
        </div>
    </div>
</template>

<style scoped>

</style>
