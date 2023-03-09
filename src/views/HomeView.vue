<script setup>
import HomeCard from '../components/HomeCard.vue';
</script>

<template>
    <div class="p-8">
        <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
            Podcast to make you smarter
        </button>
        <div class="py-1.5">
            <div class="flex items-center">
                <HomeCard image="https://picsum.photos/id/30/300/300" title="Title is here" subTitle="Subtitle is here" />
            </div>
        </div>
    </div>
</template>
