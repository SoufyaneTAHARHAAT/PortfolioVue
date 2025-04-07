<script setup>
import { ref } from 'vue';
import SingleProject from './SingleProject.vue';

let projects =ref([
    {
        name: "Voting analysis app",
        image: "deputies-analysis",
        tags: "Python; Dash; Foluim; Jupyter notebook",
        description: "Development of a political compass application that analyzes French deputies, including their votes, doctrines, and more.",
        tasks: "Data mining, data collection, and cleaning.;Clustering and classification using machine learning techniques.;Development of a reactive application using the Dash framework."
    },
    {
        name: "Finding a coach app",
        image: "find-a-coach",
        tags: "Vue.js; HTML; CSS; Javascript; Node.js",
        description: "Development of a reactive application that allows searching for a computer science teacher.",
        tasks: "Development of the app from scrach.;Using the router to navigate smoothly and easily throughout the app.;Using reusable components"
    },
    {
        name: "MoodSync",
        image: "moodsync_logo",
        tags: "Vue.js; SpringBoot; Postgresql",
        description: "Development of a social network that analyzes data to provide real-time and relevant solutions tailored to the user's mood.",
        tasks: "Development of the app from scrach.;Analysis of posts, interactions on social media, and favorite music using Artificial Intelligence.;Using APIs to provide real time solutions such as movies, activities in the area etc."
    }
]);

</script>

<template>
    <div id="projects">
        <h2 class="text-highlight-1 section-title"> Some Of My projects</h2>
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