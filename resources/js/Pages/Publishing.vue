<script setup lang="ts">

import MainLayout from "@/Layouts/MainLayout.vue";
import {Head} from "@inertiajs/vue3";
</script>

<template>
    <Head title="প্রকাশনী"/>
    <MainLayout>

        <h1 class='text-[30px] text-center text-white mt-10'> Inclusive Government: A Road To Nations Peace And Security </h1>
        <div class="flex justify-center mt-4">
        <a href="/download-pdf" class="mt-4 inline-block bg-blue-600 w-96 flex justify-center text-center text-white px-4 py-2 rounded hover:bg-blue-700 transition">
            Download PDF
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3 16.5v2.25A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75V16.5M16.5 12 12 16.5m0 0L7.5 12m4.5 4.5V3" />
            </svg>
        </a>
        </div>

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
