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
a {
    margin-left: 10px;
  display: inline-block;
  transition: transform 0.3s ease, filter 0.3s ease;
}

a:hover {
  transform: scale(1.2);
  filter: brightness(1.3);
}

.social-img {
  display: block;
  transition: transform 0.3s ease;
}


</style>