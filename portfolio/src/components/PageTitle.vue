<script setup>
    import SocialIcon from './SocialIcon.vue';
</script>

<template>
    <div id="top-line">
        <img id="profile-img" src="../assets/circledId.png" alt="Soufyane TAHARHAAT" width="300px" height="300px">
        <div id="line">
            <p>Je suis <span class="text-highlight-1">Soufyane TAHARHAAT</span>,
            <br> passionné d'informatique.</p>
            <div id="social">
                <social-icon link="https://www.linkedin.com/in/soufyane-taharhaat-253156289/" 
                img="icons8-linkedin-48"
                alt="linkedIn"></social-icon>
                <social-icon link="https://github.com/SoufyaneTAHARHAAT" 
                img="icons8-github-48"
                alt="github"></social-icon>
                <social-icon link="https://www.instagram.com/soufyane_art/" 
                img="icons8-instagram-48"
                alt="instagram"></social-icon>
            </div>
        </div>
        
    </div>
    
</template>

<style scoped>

#top-line {
    margin-top: 50px;
    width: 100%;
    height: 300px;
}

#top-line #profile-img {
    float: left;
    margin-right: 50px;
}

#top-line #line {
    float: left;
    transform: translateY(40%);
    text-align: center;
}

#top-line p {
    color: azure;
    font-size: 42px;
    line-height: 60px;
}

#tope-line p span {
    font-weight: bold;
}

#social {
    margin-top: 15px;
}


@media screen and (max-width: 905px) {
    #top-line {
        height: auto;
        text-align: center;
    }

    #top-line #profile-img {
        float: none;
        margin: 0 auto 20px;
        display: block;
    }

    #top-line #line {
        float: none;
        transform: translateY(0);
    }

    #top-line p {
        font-size: 32px;
        line-height: 48px;
    }
}
</style>