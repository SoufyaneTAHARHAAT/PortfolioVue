<script setup>
import { ref } from 'vue';

    let activeBloc= ref(0);

    const experiences = ref([
        {
            title: 'Software developer',
            date: '3 months',
            line1: "This is the first line",
            line2: "This is the second line",
            line3: "This is the third line"
        },
        {
            title: 'Web developer',
            date: '4 months',
            line1: "This is the first web line",
            line2: "This is the second web line",
            line3: "This is the third web line"
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
            <p :class="activeBloc === 0 ? 'active' : ''" class="company fw600" @click="showExp(0)">FinaTech Systems</p>
            <p :class="activeBloc === 1 ? 'active' : ''" class="company fw600" @click="showExp(1)">Nibrass</p>
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