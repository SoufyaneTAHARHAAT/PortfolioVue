<script setup>
import { ref } from 'vue';

    let activeBloc= ref(0);

    const experiences = ref([
        {
            title: 'Web developer',
            date: '3 months',
            line1: "Improvement of Al Barid Bank's official website.",
            line2: "Optimization of the 'appointment booking' feature.",
            line3: "Development and integration of reusable components in Vue.js."
        },
        {
            title: 'Web developer',
            date: '3 months',
            line1: "Collaborate with the team to implement new features and improve existing ones for clients using modern frameworks like Vue.js and React",
            line2: "Test and debug web applications to ensure compatibility across browsers and devices.",
            line3: "Work on integrating frontend components with backend APIs."
        }
    ]);

    const showExp = (id) => {
        activeBloc.value = id;
    };

</script>

<template>
    <div id="experiences">
        <h2 class="text-highlight-1 section-title">My experiences</h2>
        <div id="left">
            <p :class="activeBloc === 0 ? 'active' : ''" class="company fw600" @click="showExp(0)">Internship at Finatech Systems</p>
            <p :class="activeBloc === 1 ? 'active' : ''" class="company fw600" @click="showExp(1)">Internship at V5 Digital</p>
        </div>
        <div id="right">
            <template v-for="(job, index) in experiences">
                <div class="job-details" :class="index===activeBloc ? '': 'hide'" :id="'bloc_'+index">
                    <h3 class="fw600">{{ job.title }}</h3>
                    <span id="date">{{ job.date }}</span>
                    <br/>
                    <p class="fw600 mtb8" style="margin-top: 10px;"><span class="text-highlight-2">✔ </span>{{ job.line1 }}</p>
                    <p class="fw600 mtb8"><span class="text-highlight-2">✔ </span>{{ job.line2 }}</p>
                    <p class="fw600 mtb8"><span class="text-highlight-2">✔ </span>{{ job.line3 }}</p>
                </div>
            </template>
        </div>
    </div>
</template>

<style scoped>

#experiences {
    margin-top: 60px;
    color: rgb(172, 171, 171);
}

#experiences #left {
    float: left;
    width: 25%;
}

#experiences #right {
    float: right;
    width: 75%;
}

#experiences #right h3 {
    font-size: 20px;
}

.fw600 {
    font-weight: 600;
}

.mtb8 {
    margin: 8px 0px;
}

#date {
    font-style: italic;
    font-size: 14px;
}

.company {
    border-left: 4px solid var(--vt-c-custom-text-1);
    line-height: 30px;
    padding-left: 10px;
}

.active {
    border-left: 4px solid var(--vt-c-custom-text-2);
    color: var(--vt-c-custom-text-2);
}

.company:hover {
    cursor: pointer;
    color: var(--vt-c-custom-text-1);
}

.hide {
    display: none;
}

@media screen and (max-width: 600px) {
    #experiences #right {
        width: 100%;
        margin-top: 20px;
    }

    #experiences #left {
        width: 100%;
    }

    .company {
        border: none;
        padding-left: 0px;
        float: left;
        margin-right: 10px;
    }
}
</style>