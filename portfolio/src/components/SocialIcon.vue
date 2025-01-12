<script setup>

const props = defineProps({
    img: String,
    link: String,
    alt: String
});
</script>

<template>
    <a :href="props.link">
        <img class="social-img" :src="`/src/assets/${props.img}.png`" :alt="props.alt" width="36px">
    </a>
</template>

<style scoped>
.social-img {
    margin-right: 10px;
    filter: opacity(0.8);
}
</style>