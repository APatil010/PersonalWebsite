<template>
  <div class="faqsGrid">
    <Question v-for="q in questions" :key="q.id" :question="q.question" :answer="q.answer" />
  </div>
</template>

<script setup>
import Question from "./subcomponents/Question.vue";
import data from "../assets/data.js";

const questions = data.faqs;
</script>

<style scoped>
  .faqsGrid {
      display: grid;
      grid-template-columns: 1fr 2fr 1fr;

  }
</style>