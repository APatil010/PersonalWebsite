<template>
    <div class="question">
        <strong>{{props.question}}</strong>
    </div>
    <div class="answer">
        {{props.answer}}
    </div>
    <div class="separator">
        <div class="circle"></div>
        <div class="circle"></div>
        <div class="circle"></div>
    </div>
</template>

<script setup>
const props = defineProps({
    question: String,
    answer: String
});

</script>

<style scoped>
    .question,
    .answer {
        grid-column: 2 / 3;
        padding: 1em;
    }

    .answer {
        text-align: justify;
    }
    .separator {
        display: flex;
        grid-column: 2 / 3;
        justify-self: center;
    }

    .circle {
        width: 0.5em;
        height: 0.5em;
        background-color: black;
        margin: 0.25em;
        border-radius: 50%;
    }
</style>