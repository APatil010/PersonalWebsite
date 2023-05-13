<template>
    <div class="projects">
        <div v-for="p in projects" :key="p.id" class="projectCard">
            <img :src="p.src" alt="projectImage" />
            <div>
                <div class="title font-28"> {{ p.title }} </div>
                <div class="subTitle font-18"> {{ p.subtitle }} </div>
                <div class="description font-16 mono-light"> {{ p.description }} </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    import data from "../assets/data.js";
    const projects = data.projects;

</script>

<style scoped>
  .projects {
      display: grid;
      grid-template-columns: 4em 1fr 4em;
      justify-items: center;
      grid-row-gap: 2em;
  }

  .projectCard {
      grid-column: 2 / 3;
      width: 100%;
      color: black;
      border-left: 1px solid black;
      padding: 1rem;
      display: grid;
      grid-template-columns: 1fr 3fr;
      grid-row-gap: 0.25em;
  }

  .projectCard > img {
      width: 8em;
      border: 1px solid white;
      place-self: center;
  }

  .description, .title, .subTitle {
      padding-left: 2rem;
  }

  .description {
      text-align: justify;
  }
</style>

