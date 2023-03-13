<script setup>
import Play from 'vue-material-design-icons/Play.vue';
import Pause from 'vue-material-design-icons/Pause.vue';
import DotsHorizontal from 'vue-material-design-icons/DotsHorizontal.vue';
import Heart from 'vue-material-design-icons/Heart.vue';
import ClockTimeThreeOutline from 'vue-material-design-icons/ClockTimeThreeOutline.vue';

import artist from '../artist.json';
</script>

<template>
    <div class="p-8">
        <button type="button" class="text-white text-2xl font-semibold hover:underline cursor-pointer">
            {{ artist.name }}
        </button>
        <div class="py-1.5"></div>
        <div class="flex items-center w-full relative h-full">
            <img width="140" :src="artist.albumCover">
            <div class="w-full ml-5">
                <div style="font-size: 33px;"
                    class="text-white absolute w-full hover:underline cursor-pointer top-0 font-semibold">
                    {{ artist.name }}
                </div>
                <div class="text-gray-300 text-[13px] flex">
                    <div class="flex">Album</div>
                    <div class="ml-2 flex">
                        <div class="circle mt-2 mr-2"></div>
                        <span class="-ml-0.5">{{ artist.releaseYear }}</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.circle {
    width: 4px;
    height: 4px;
    background-color: rgb(189, 189, 189);
    border-radius: 100%;
}
</style>