<script setup>
 import SocialIcons from './SocialIcons.vue';
</script>

<template>
    <div id="top-line">
        <img id="profile-img" src="../assets/me.png" alt="me" width="300px" height="300px">
        <div id="line">
            <p>Je suis <span class="text-highlight-1">Francky RAKOTONIRINA</span>, <br/>
                Développeur Php
            </p>
            <div id="social">
                <SocialIcons img="git" alt="github" link="https://github.com/Francky-Faniry" />
                <SocialIcons img="in" alt="linkedin" link="https://www.linkedin.com/in/francky-faniry-rakotonirina-989324267/" />
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
        float: left; /*pour le faire coller à gauche */
        margin-right: 50px;
    }

    #top-line #line {
        float:left;
        transform: translateY(40%); /*pour faire un decalage sur l'axe Y de 40%*/
        text-align: center; /*pour centrer le texte */
    }

    #top-line p {
        font-size: 42px;
        line-height: 60px;
    }

    #top-line p span {
        font-weight: bold;
    }

    #social {
        margin-top: 15px;
    }

    @media screen and (max-width: 905px) {
        #top-line #profile-img {
            display:none;
        }

        #top-line #line {
            float:none;
            transform: translateY(0%);
        }

        #top-line p {
            font-size: 36px;
        }
    }
</style>
