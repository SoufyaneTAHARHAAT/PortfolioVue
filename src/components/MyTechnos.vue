<script setup>
</script>

<template>
    <div id="skills">
        <h2 class="text-highlight-1 section-title">My Tech Toolbox</h2>
        <div id="icons-list">
            <div class="techno-container">
                <i class="techno-icon devicon-html5-plain"></i>
                <br><span>HTML</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-css3-plain"></i>
                <br><span>CSS</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-javascript-plain"></i>
                <br><span>Javascript</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-typescript-plain"></i>
                <br><span>Typescript</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-angular-plain"></i>
                <br><span>Angular</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-vuejs-plain"></i>
                <br><span>Vuejs</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-react-original"></i>
                <br><span>React</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-nodejs-plain"></i>
                <br><span>Nodejs</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-express-original"></i>
                <br><span>Expressjs</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-postgresql-plain"></i>
                <br><span>Postgresql</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-spring-original"></i>
                <br><span>Springboot</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-docker-plain"></i>
                <br><span>Docker</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-python-plain"></i>
                <br><span>Python</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-java-plain"></i>
                <br><span>Java</span>
            </div>
            <!-- <div class="techno-container">
                <i class="techno-icon devicon-cplusplus-plain"></i>
                <br><span>C++</span>
            </div> -->
            <div class="techno-container">
                <i class="techno-icon devicon-kubernetes-plain"></i>
                <br><span>Kubernetes</span>
            </div>
            <div class="techno-container">
                <i class="techno-icon devicon-sonarqube-original"></i>
                <br><span>Sonarqube</span>
            </div>
        </div>
    </div>
</template>

<style scoped>
#skills {
    margin-top: 60px;
}

#icons-list {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    grid-template-rows: repeat(2, 1fr);
    grid-column-gap: 5px;
    grid-row-gap: 50px;
    margin-top: 35px;
}

.techno-container {
    text-align: center;
    color: var(--vt-c-custom-text-1);
    transition-duration: 0.5s;
}

.techno-container span {
    font-weight: bold;
}

.techno-container:hover {
    transform: rotate(15deg);
    color: var(--vt-c-custom-text-2);
}

.techno-icon {
    font-size: 80px;
    margin: 0 auto;
    color: var(--vt-c-custom-text-1);
}

.techno-icon:hover {
    color: var(--vt-c-custom-text-2);
    transform: rotate(15deg);
}

@media screen and (max-width: 905px) {
    #icons-list {
        grid-template-columns: repeat(4, 1fr);
        grid-template-rows: repeat(4, 1fr);
        grid-column-gap: 5px;
        grid-row-gap: 40px;
    }
}

@media screen and (max-width: 450px) {
    #icons-list {
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: repeat(7, 1fr);
        grid-column-gap: 5px;
        grid-row-gap: 20px;
    }
}

</style>