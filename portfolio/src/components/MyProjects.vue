<script setup>
import { ref } from 'vue';
import SingleProject from './SingleProject.vue';

let projects =ref([
    {
        name: "project 1",
        image: "imagesP",
        tags: "Python; HTML; CSS; Javascript",
        description: "this is the decription of the first project",
        tasks: "task1.;task2.;task3"
    },
    {
        name: "project 2",
        image: "imagesP",
        tags: "Python; HTML; CSS; Javascript",
        description: "this is the decription of the first project",
        tasks: "task1.;task2.;task3"
    },
    {
        name: "project 3",
        image: "imagesP",
        tags: "Python; HTML; CSS; Javascript",
        description: "this is the decription of the first project",
        tasks: "task1.;task2.;task3"
    },
    {
        name: "project 4",
        image: "imagesP",
        tags: "Python; HTML; CSS; Javascript",
        description: "this is the decription of the first project",
        tasks: "task1.;task2.;task3"
    },
    {
        name: "project 5",
        image: "imagesP",
        tags: "Python; HTML; CSS; Javascript",
        description: "this is the decription of the first project",
        tasks: "task1.;task2.;task3"
    },
    {
        name: "project 6",
        image: "imagesP",
        tags: "Python; HTML; CSS; Javascript",
        description: "this is the decription of the first project loremmmmmmmmmmmmmmme eeeeee e er errrqzef ezfef efefqef fsfef vd d  scs fs  ssdsf eesc qsre dvsdvc trtbr ss vvvv",
        tasks: "task1.;task2.;task3"
    }
]);

</script>

<template>
    <div id="projects">
        <h2 class="text-highlight-1 section-title">My projects</h2>
        <single-project v-for="(project, index) in projects" :key="project.name"
        :project="project" :reverse="index % 2 ===0 ? false : true"/>
    </div>
</template>

<style scoped>

#projects {
    display: inline-block;
    margin-top: 80px;
    color: rgb(172, 171, 171);
}
</style>