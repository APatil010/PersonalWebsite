<template>
    <div class="skills">
        <h3 class="skillHeader"> Skills </h3>
          <div v-for="skill in skills" class="skill">
              <div class="skillText">{{skill.name}}</div>
              <div class="progressBar">
                  <div class="actualProgress" :style="{ width: skill.progress + '%' } "></div>
              </div>
          </div>
    </div>
</template>

<script setup>
import data from "../../assets/data.js";
const skills = data.skills;
</script>

<style scoped>
  .skills {
      grid-column: 2 / 3;
      display: grid;
      grid-template-columns: 1fr 1fr;
  }

  .skillHeader {
      text-align: center;
      grid-column: 1 / 3;
  }

  .skill {
      display: grid;
      grid-template-columns: 3fr 2fr;
      align-content: center;
  }

  .skill > * {
      margin: 0.75em;
  }

  .progressBar {
      height: 1em;
      background-color: gray;
  }

  .actualProgress {
      height: 1em;
      background-color: black;
  }
</style>