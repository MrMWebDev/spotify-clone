<script setup>
import { ref, toRefs, watchEffect } from 'vue';
import { useRoute } from 'vue-router';

const route = useRoute();

const props = defineProps({
    iconString: String,
    iconSize: Number,
    pageUrl: String,
    name: String
});
const { iconString, iconSize, pageUrl, name } = toRefs(props);

let icon = ref(null);
let textIsHover = ref(false);

watchEffect(() => {
    if (route.path == pageUrl.value) {
        icon.value = iconString.value + '-active';
        textIsHover.value = true;
    } else {
        icon.value = iconString.value + '-inactive';
        textIsHover.value = false;
    }
});

const isHover = () => {
    if (icon.value === iconString.value + '-active') return;

    if (icon.value === iconString.value + '-inactive') {
        icon.value = iconString.value + '-inactive-hover';
        textIsHover.value = true;

    } else {
        icon.value = iconString.value + '-inactive';
        textIsHover.value = false;
    }
};
</script>

<template>
    <li class="flex items-center justify-start pb-4 cursor-pointer" @mouseenter="isHover()" @mouseleave="isHover()">
        <img :width="iconSize" src="`/public/images/icons/${icon}.png`" alt="">
        <div></div>
    </li>
</template>

<style lang="scss" scoped></style>