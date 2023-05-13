<template>
    <div class="aboutGrid">
        <div class="aboutImage">
            <img :src="MyPhoto" alt="My Photo" />
        </div>
        <div class="aboutText">
            <p>
                My expertise lies in  front-end design and development.
                My passion to make this world sophisticated with simple
                design and intersection of technology, has allowed me
                to enjoy my work and focus around the Front-end Development
                and design. This goal of mine was carried throughout my
                undergraduate and my graduate program to  intensively
                study this area of computer  science. Currently, I am
                open to job opportunities to put my skills to test in
                real world, and make my impact for better growth as a
                developer.
            </p>
        </div>
        <div class="aboutStatus">
            <div class="status font-20">
                Status:
            </div>
            <p>
                Full Stack Software Engineer at Impact.com
            </p>
        </div>
        <Skills />
    </div>
</template>

<script setup>
import MyPhoto from "../assets/my_photo.png";
import Skills from "./subcomponents/Skills.vue";

</script>

<style scoped>
    .aboutGrid {
        min-height: 100vh;
        display: grid;
        grid-template-columns: 1fr 3fr 1fr;
        grid-row-gap: 1em;
    }

    .aboutImage, .aboutText, .aboutStatus {
        grid-column: 2 / 3;
        justify-self: center;
    }
    .aboutImage > img {
        width: 169px;
        height: 218px;
        border-radius: 10%;
        border: 2px solid black;
        padding: 5px;
    }
</style>