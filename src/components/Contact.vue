<template>
    <div class="contactGrid">
        <div class="message">
            <h2><strong>Want to say Hello?</strong></h2>
            <p>Do you have any job opportunity as software developer or project idea to work on, or just talk about something interesting in tech, write me an email.</p>
        </div>

        <div class="gmail">
            <FontAwesomeIcon :icon="faEnvelope" size="3x" />
            <p><strong><a href="mailto:patilaarsh@gmail.com" target="_blank">patilaarsh@gmail.com</a></strong></p>
        </div>

        <div class="linkedin">
            <FontAwesomeIcon :icon="faLinkedin" size="3x" />
            <p><strong><a href="https://linkedin.com/in/aarshpatil" target="_blank">https://linkedin.com/in/aarshpatil</a></strong></p>
        </div>

        <div class="social-section">
            <h2> I am also Social...</h2>
            <div class="social-icons">
                <a href="https://facebook.com/aarsh.patil" target="_blank">
                    <FontAwesomeIcon :icon="faFacebook" size="3x" />
                </a>
                <a href="https://twitter.com/apatil010" target="_blank">
                    <FontAwesomeIcon :icon="faTwitter" size="3x" />
                </a>
                <a href="https://instagram.com/the.vegan.jedi" target="_blank">
                    <FontAwesomeIcon :icon="faInstagram" size="3x" />
                </a>
                <a href="https://codepen.io/AarshPatil" target="_blank">
                    <FontAwesomeIcon :icon="faCodepen" size="3x" />
                </a>
                <a href="https://bitbucket.org/Ashter31/" target="_blank">
                    <FontAwesomeIcon :icon="faBitbucket" size="3x" />
                </a>
                <a href="https://github.com/apatil010" target="_blank">
                    <FontAwesomeIcon :icon="faGithub" size="3x" />
                </a>
                <a href="https://medium.com/techie-js" target="_blank">
                    <FontAwesomeIcon :icon="faMedium" size="3x" />
                </a>
            </div>
        </div>
    </div>
</template>

<script setup>
    import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
    import { faCodepen, faLinkedin, faFacebook, faTwitter, faInstagram, faGithub, faBitbucket, faMedium } from '@fortawesome/free-brands-svg-icons';
    import { faEnvelope } from '@fortawesome/free-solid-svg-icons';
</script>

<style scoped>
    .contactGrid {
        min-height: 100vh;
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-row-gap: 3em;
        grid-template-rows: repeat(3, min-content);
    }

    .message, .social-section {
        grid-column: 1 / 3;
    }

    .message {
        margin: 3rem;
    }

    .social-section {
        text-align: center;
    }

    .gmail, .linkedin {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 1em;
    }

    .gmail > p, .linkedin > p {
        margin-left: 2rem;
    }

    .social-icons {
        display: flex;
        justify-content: center;
    }

    .social-icons > * {
        padding: 1em;
    }
</style>