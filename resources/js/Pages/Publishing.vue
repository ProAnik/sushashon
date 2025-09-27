<script setup lang="ts">

import MainLayout from "@/Layouts/MainLayout.vue";
import {Head} from "@inertiajs/vue3";
</script>

<template>
    <Head title="প্রকাশনী"/>
    <MainLayout>
        <div class="w-full mt-10 h-[80vh] border rounded-lg overflow-hidden shadow">
            <iframe
                src="/inclusive_gov.pdf"
                class="w-full h-full"
                type="application/pdf"
            ></iframe>
        </div>
    </MainLayout>
</template>

<style scoped>

</style>
