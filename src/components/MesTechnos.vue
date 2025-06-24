<script setup>
  
</script>

<template>
    <div id="skills">
        <h2 class="text-highlight-1 section-title">Mes technos préférées</h2>
        <div id="icons-list">
            <div class="techno-container"><i class="techno-icon devicon-html5-plain"></i> <br/> <span>HTML</span></div>
            <div class="techno-container"><i class="techno-icon devicon-css3-plain"></i> <br/> <span>Css</span></div>
            <div class="techno-container"><i class="techno-icon devicon-php-plain"></i> <br/> <span>Php</span></div>
            <div class="techno-container"><i class="techno-icon devicon-javascript-plain"></i> <br/> <span>Javascript</span></div>
            <div class="techno-container"><i class="techno-icon devicon-laravel-plain"></i> <br/> <span>Laravel</span></div>
            <div class="techno-container"><i class="techno-icon devicon-vuejs-plain"></i> <br/> <span>VueJS</span></div>
            <div class="techno-container"><i class="techno-icon devicon-wordpress-plain"></i> <br/> <span>Wordpress</span></div>
            <div class="techno-container"><i class="techno-icon devicon-git-plain"></i> <br/> <span>Git</span></div>
        </div>
    </div>
</template>

<style scoped>
   #skills {
        margin-top: 60px;
   }

   #icons-list {
        display: grid; /*pour créer une grille */
        grid-template-columns: repeat(4, 1fr); /*grille de 8 colonne*/
        grid-template-rows: repeat(2, 1fr); /*grille de 2 ligne*/
        grid-column-gap: 5px; /*espace entre les colonne*/
        grid-row-gap: 50px;/*espace entre les lignes*/
        margin-top: 35px;
   }

   .techno-container {
        text-align: center; /*pour centrer le text*/
        color: var(--vt-c-custom-text-1);
        transition: transform 0.5s; /*petite effet lors de la survol de la souris pour chnager la couleur et l'orientation de l'icon*/
   }

   .techno-container span {
        font-weight: bold; /*text en gras*/
   }

   /*au survol de la souris*/
   .techno-container:hover {
        transform: rotate(15deg); /*rotation de 15 dégré*/
        color: var(--vt-c-custom-text-2);
   }

   .techno-icon {
        font-size: 80px;
        margin: 0 auto; /*centrer l'icon*/
        color: var(--vt-c-custom-text-1); /*colorer l'icon*/
   }

   .techno-icon:hover {
        color: var(--vt-c-custom-text-2);
        transform: rotate(15deg);
   }

   @media screen and (max-width: 905px) {
       #icons-list {
            display: grid; /*pour créer une grille */
            grid-template-columns: repeat(4, 1fr); /*grille de 8 colonne*/
            grid-template-rows: repeat(4, 1fr); /*grille de 2 ligne*/
            grid-column-gap: 5px; /*espace entre les colonne*/
            grid-row-gap: 40px;/*espace entre les lignes*/
        } 
   }

   @media screen and (max-width: 450px) {
        #icons-list {
            display: grid; /*pour créer une grille */
            grid-template-columns: repeat(2, 1fr); /*grille de 8 colonne*/
            grid-template-rows: repeat(8, 1fr); /*grille de 2 ligne*/
            grid-column-gap: 5px; /*espace entre les colonne*/
            grid-row-gap: 20px;/*espace entre les lignes*/
        }
   }
</style>