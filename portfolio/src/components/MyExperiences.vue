<script setup>
import { ref } from 'vue';


    const infos = ref([
        {
            jobTitle: 'Software developer',
            period: '3 months',
            tasks: ['task1', 'task2', 'task3']
        },
        {
            jobTitle: 'Web developer',
            period: '3 months',
            tasks: ['task11', 'task22', 'task33']
        }
    ]);

    const index = ref(0);

</script>

<template>
    <div id="experiences">
        <h2 class="text-highlight-1 section-title">My experiences</h2>
        <div id="left">
            <p class="company fw600" @click="index=0">FinaTech Systems</p>
            <p @click="index=1">Company 2</p>
        </div>
        <div id="right">
            
        </div>
    </div>
</template>

<style scoped>

</style>