<script setup>
import CategorySelect from '../components/CategorySelect.vue';
</script>

<template>
    <div class="p-8">
        <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
            Recommended Radios
        </button>
        <div class="py-1.5">
            <div class="flex items-center">
                <CategorySelect category="Podcasts" image="https://picsum.photos/id/40/300/300" />
            </div>
        </div>
    </div>
</template>