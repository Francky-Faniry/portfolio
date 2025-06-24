<script setup>
    import { ref } from 'vue';

    let activeBloc = ref(0)

    let experiences = ref([
        {
            title: "Développeur Php/Laravel",
            date: "Depuis Décembre 2024",
            line1: "Conception de la partie backend",
            line2: "Mise en place du deploiement dans o2switch",
            line3: "Suivi des tâches faites par les stagiaires"
        }, 
        {
            title: "Stagiaire Php/Laravel",
            date: "Juillet 2024 - Décembre 2024",
            line1: "Conception de la partie backend"
        }, 
    ]);

    const ShowXp = (id) => {
        activeBloc.value = id;
    };
</script>

<template>
    <div id="xp">
        <h2 class="text-highlight-1 section-title">Expériences</h2>
        <div id="left">
            <p :class="activeBloc === 0 ? 'active' : ''"class="company fw600" @click="ShowXp(0)">GasikaraDigital</p>
            <p :class="activeBloc === 1 ? 'active' : ''"class="company fw600" @click="ShowXp(1)">GasikaraDigital</p>
        </div>
        <div id="right">
            <template v-for="(job,index) in experiences">
                <div class="job-details" :class="index === activeBloc ? '' : 'hide'" :id="'bloc_'+index">
                    <h3 class="fw600">{{ job.title }} </h3>
                    <span id="date">{{ job.date }} </span>
                    <br/>
                    <h3 class="fw600 mtb8" style="margin-top: 10px;"><span class="text-highlight-2">✓</span>{{ job.line1 }} </h3>
                </div>
            </template>
        </div>
    </div>
</template>

<style scoped>
    #xp {
        margin-top: 60px;
    }

    #xp #left {
        float: left;
        width: 25%;
    }

    #xp #right {
        float: left;
        width: 75%;
    }

    #xp #right h3 {
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
        border-left: 4px solid var(--vt-c-custom-tetx-1); /*pour collorer la partie gauche de la société*/
        line-height: 30px;/*pour espacer les société*/
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

    @media screen and (max-width:600px) {
        #xp #right {
            width: 100%;
            margin-top: 20px;
        }

        #xp #left {
            width: 100%
        }

        .company {
            border: none;
            padding-left: 0px;
            float: left;
            margin-right: 10px;
        }
    }
</style>
