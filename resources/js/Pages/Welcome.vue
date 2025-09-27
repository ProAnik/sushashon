<script setup>
import { Head, Link } from '@inertiajs/vue3';
import MainLayout from "@/Layouts/MainLayout.vue";

</script>

<template>
    <Head title="Welcome" />
    <MainLayout>
        <div class="w-full flex justify-center my-8">
            <img src="/images/banner.jpeg" class="lg:max-w-xl sm:w-full" alt="">
        </div>

        <div class="text-white leading-[1.5] text-2xl lg:text-3xl text-center pb-24">
            ন্যায় বিচার ভিত্তিক সমাজ ব্যবস্হা গঠনের মাধ্যমে দেশে সু-শাসন কায়েম করাই আমাদের লক্ষ্য! জনগনের মধ্যে শৃংখলা,
            ও তাদের নিরাপত্তা নিশ্চিতের মাধ্যমেই সমাজ তথা দেশে শান্তি প্রতিস্ঠা করাই আমাদের মুল উদ্দেশ্য।
        </div>
    </MainLayout>

</template>
